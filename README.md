# Find-the-Distinct-Difference-Array
class Solution:
    def distinctDifferenceArray(self, nums: List[int]) -> List[int]:
        if nums is None:
            return None
        n=len(nums)
        d=[]
        for i in range(n):
            s=[]
            p=[]
            for j in range(i+1):
                p.append(nums[j])
            for j in range(i+1,n):
                s.append(nums[j])
            d.append(len(set(p))-len(set(s)))
        return d
