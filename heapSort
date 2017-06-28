class Solution {
public:
	void heapSort(vector<int>& nums) { // using min heap
		int n = nums.size();
		// first build the heap by percolating up one by one, i.e., insertion one by one
		buildHeap(nums); // takes nlogn
						 // now sort by replacing the last element with the root
						 // then heapify by percolating down
		for (int i = n - 1; i > 0; i--) {
			swap(nums[i], nums[0]);
			percolateDown(nums, i - 1); // heapify from nums[0] to nums[i-1], percolating down
		}
		reverse(nums.begin(), nums.end());
	}

	void swap(int& a, int& b) {
		int temp = a;
		a = b;
		b = temp;
	}

	void buildHeap(vector<int>& nums) {
		for (int i = 1; i < nums.size(); i++) {
			int pos = i;
			// insert nums[i] to heap{nums[0], nums[i-1]}
			while (pos > 0) {
				int parentPos = (pos - 1) / 2;
				if (nums[pos] < nums[parentPos])
					swap(nums[pos], nums[parentPos]);
				pos = parentPos;
			}
		}
	}

	void percolateDown(vector<int>& nums, int endPos) {
		int pos = 0;
		while (pos < endPos) {
			int leftChildPos = 2 * pos + 1;
			int rightChildPos = leftChildPos + 1;
			if (leftChildPos > endPos) return; // already a leaf
			int minPos;
			if (rightChildPos > endPos) minPos = leftChildPos;
			else minPos = nums[leftChildPos] < nums[rightChildPos] ? leftChildPos : rightChildPos;
			if (nums[pos] > nums[minPos]) {
				swap(nums[pos], nums[minPos]);
				pos = minPos;
			}
			else return;
		}
	}
};

int main() {
	vector<int> nums{ 76,7,3,90,6};
	Solution sol;
	sol.heapSort(nums); // in ascending order
	for (int i = 0; i < nums.size(); i++) cout << nums[i] << " ";
	return 0;
}
