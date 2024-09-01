class Solution {
public:
    int maxPathSum(vector<int>& nums1, vector<int>& nums2) {
        int n = nums1.size();
        int m = nums2.size();
        int i = 0, j = 0;
        int sum1 = 0, sum2 = 0, result = 0;

        while (i < n && j < m) {
            if (nums1[i] == nums2[j]) {
                result += max(sum1, sum2) + nums1[i];
                sum1 = 0;
                sum2 = 0;
                i++;
                j++;
            } else if (nums1[i] < nums2[j]) {
                sum1 += nums1[i];
                i++;
            } else {
                sum2 += nums2[j];
                j++;
            }
        }

        // Add remaining elements from nums1 or nums2
        while (i < n) {
            sum1 += nums1[i++];
        }
        while (j < m) {
            sum2 += nums2[j++];
        }

        // Add the maximum of the remaining sums to the result
        result += max(sum1, sum2);

        return result;
    }
};
