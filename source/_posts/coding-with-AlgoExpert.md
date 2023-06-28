---
title: coding_with_AlgoExpert
date: 2020-11-29 13:37:41
tags: Array
---

1. Two Number Sum
   Method: unordered_set O(n) time, O(n) space due to container set; 
   double pointer O(nlogn)  time, O(1);
   O(1) < O(logn) < O(n) < O(nlogn) In computers, it's log base 2 and not base 10. 

{% codeblock %}
   vector<int> twoNumberSum(vector<int> array, int targetSum) {
  // set instead of hashmap,because unrelated the position of element
	unordered_set<int> uSet;
	for(auto ele:array){ //instead of input firstly then find
		if (uSet.find(targetSum-ele)!=uSet.end())
			 return {ele,targetSum-ele};// can return two elements with the method
		else
					uSet.insert(ele);
	}

  return {};
}
{% endcodeblock %}


2. Validate Subsequence
   Description:unnessarily adjacent in the array but in the same order
   Method:  rapid and slow pointer  O(n) time, O(1) space
{% codeblock %}
   bool isValidSubsequence(vector<int> array, vector<int> sequence) {
  // rapid and slow pointer
	int arrIndex=0;
	int seqIndex=0;

		while(arrIndex<array.size() && seqIndex< sequence.size()){
			if(sequence[seqIndex]==array[arrIndex])
			  	seqIndex++;
			arrIndex++;
				
		}
  return seqIndex==sequence.size();
}
{% endcodeblock %}

3. Three Number Sum 
   Method: triple pointer  O(n^2) time, O(n) space

4. Smallest Difference
   Method: double pointer( rapid and slow pointer)  O(nlog(n)+mlog(m)) time, O(1) space
{% codeblock %}
   vector<int> smallestDifference(vector<int> arrayOne, vector<int> arrayTwo) {
  //double pointers
	sort(arrayOne.begin(),arrayOne.end());
	sort(arrayTwo.begin(),arrayTwo.end());
	vector<int> res;
	int abs_val=INT_MAX;
	int arroneidx=0;
	int arrtwoidx=0;
	while(arroneidx<arrayOne.size() && arrtwoidx<arrayTwo.size()){
		if(abs(arrayOne[arroneidx]-arrayTwo[arrtwoidx])<abs_val){
						abs_val=abs(arrayOne[arroneidx]-arrayTwo[arrtwoidx]);
			       res={arrayOne[arroneidx], arrayTwo[arrtwoidx]};
		}
		
		if(arrayOne[arroneidx]<arrayTwo[arrtwoidx]){
			 arroneidx++;
		}else if(arrayOne[arroneidx]>arrayTwo[arrtwoidx]){
				arrtwoidx++;
		}else{
			return {arrayOne[arroneidx], arrayTwo[arrtwoidx]};
		}
	}
  return res;
}
{% endcodeblock %}

5. Move Element To End (mutate original array)
   Method: double pointer O(n) time, O(1) space
{% codeblock %}
   vector<int> moveElementToEnd(vector<int> array, int toMove) {
  // double pointer
	int frontIdx=0;
	int tailIdx=array.size()-1;
	while(frontIdx<tailIdx){
		if(array[frontIdx]==toMove){
			 swap(array[frontIdx],array[tailIdx]);
			 tailIdx--;
		}else{
			frontIdx++;
		}
	}
  return array;
}
{% endcodeblock %}

6. Monotonic Array
  Method:judge if neither no-decrease nor no-increase O(n) time, O(1) space
{% codeblock %}
  bool isMonotonic(vector<int> array) {
  // 
	if(array.size()<=2) 
		return true;
	bool isNonInc=true;
	bool isNonDec=true;
	for(int i=0;i<array.size()-1;i++){
		if(array[i]>array[i+1])
			isNonDec=false;
		if(array[i]<array[i+1])
			isNonInc=false;
	}
  return isNonDec || isNonInc;
}
{% endcodeblock %}

7.spiral traverse

8.Array of Products
 Method:the product with the ele as centre divided into left and right part   O(n) time, O(n) space
{% codeblock %}
 vector<int> arrayOfProducts(vector<int> array) {
  // Write your code here.
	int froPro=1;
	int tailPro=1;
	vector<int> froProArr(array.size(),1);
	vector<int> tailProArr(array.size(),1);
	vector<int> res(array.size(),1);
	for(int i=0;i<array.size()-1;i++){
				 froProArr[i+1]=froProArr[i]*array[i];
	}
	
	for(int i=array.size()-1;i>0;i--){
				 tailProArr[array.size()-i]= tailProArr[array.size()-i-1]*array[i];
	}
	for(int i=0;i<array.size();i++){
				 res[i]=froProArr[i]*tailProArr[array.size()-1-i];
	}
  return res;
}
{% endcodeblock %}

9.Four Number Sum
  Method: 1.four pointer two loop  O(n^3) time, O(??) space
          2. divide into two two_sum and with map to store the pair numbers and their sum  O(average n^2) time, O(n^2) space

{% codeblock %}
  vector<vector<int>> fourNumberSum(vector<int> array, int targetSum) {
  vector<vector<int>> res;
	sort(array.begin(),array.end());
	for(int i=0;i<array.size();i++)
	  for(int j=i+1;j<array.size();j++){
			  int targetSum_two=targetSum-array[i]-array[j];
        int leftPoi=j+1;
			  int rigPoi=array.size()-1;
			  while(leftPoi<rigPoi){
					int sumTwo=array[leftPoi]+array[rigPoi];
					if(sumTwo<targetSum_two){
						leftPoi++;
					}else if(sumTwo>targetSum_two){
						 rigPoi--;
					}else{
						res.push_back({array[i],array[j],array[leftPoi],array[rigPoi]});
						leftPoi++;
						rigPoi--;
					}
				}
		}	  	
  return res;
}
{% endcodeblock %}

10. Subarray Sort




11.
    vector<int> count(IndexMax=size() rather than size()-1, 0);
     vector<int>  vec;
     	the last element=*(vec.end()-1);












08.03.2021
// how to jump out of double loops in tri loops	