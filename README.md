##  First, the principle of the algorithm 

###   1. Overview of the principle 

![avatar]( 20210307124845583.png) 

   Internal Shape Descriptor (ISS) is a method to represent solid geometry. The algorithm contains rich geometric feature information and can complete high-quality point cloud registration. Set a point in the point cloud, and the specific process of extracting key points is as follows: 1. Establish a local coordinate system for each point in the point cloud and set a search radius for all points;  

2. Determine that each point in the point cloud is centered and is all points within the radius area, and calculate the weights of these points, the expression of which is: 3. Calculate the covariance matrix for each point: 4. Calculate the eigenvalues {} of the covariance matrix for each point and arrange them in order from largest to smallest; 5. Select the key points according to the following rules. The significance feature is the smallest eigenvalue: The value of usually does not exceed 1. The basic principle is to avoid detecting key points at points where similar diffusion occurs along the main direction. Since a repeatable standard reference frame cannot be established, it is difficult for the subsequent description stage to produce an effect. In the remaining points, the significance depends on the size of the smallest eigenvalue. Non-maximum suppression () is performed on the significant features within the set radius, and the points with large changes in the main direction are reserved as key points. 

###   2. References 

>  [1] Zhong Y. Intrinsic shape signatures: A shape descriptor for 3D object recognition [C]//IEEE International Conference on Computer Vision Workshops. IEEE, 2010. [2] Li Renzhong, Yang Man, Tian Yu, Liu Yangyang, Zhang Yanluan. Point cloud registration algorithm based on ISS feature points combined with improved ICP [J]. Advances in Laser and Optoelectronics, 2017, 54 (11): 312-319. [3] Ge Baozhen, Zhou Tianyu, Chen Lei, Tian Qingguo. Point cloud splicing method based on improved ISS feature points and artificial bee colony algorithm [J]. Journal of Tianjin University (Natural Science and Engineering Technology Edition), 2016, 49 (12): 1296-1302. [4] Li Yuxiang, Guo Jiming, Pan Shangyi, Lu Lili, Lu Zhuxing, Zhang Di. A point cloud registration algorithm based on IS-SHOT features [J]. Bulletin of Surveying and Mapping, 2020 (04): 21-26. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957454277
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957454277
 ```  
![avatar]( 021d71f2f32c45cbb8b7aa2919dd323c.png) 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  See: Chapter 6 of Error Theory and Foundations of Measurement Adjustment 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574556591
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574556591
 ```  


--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  See: PCL Kmeans point cloud clustering 

##  Code implementation 

KMeans.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574557011
 ```  
KMeans.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574557011
 ```  
main.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574557011
 ```  
##  III. Display of results 

###  1. Primitive point cloud 

![avatar]( a26324dda05a4e948f2c794366208e46.png) 

###  2. Clustering results 

![avatar]( 3109750bdb724a8489728e630929ac4d.png) 



--------------------------------------------------------------------------------

##  I. Overview 

![avatar]( 0b2c490602bb4429ae76ff1d0af7d9f7.jpeg) 

    As shown by the blue line in the figure below, for any query point, the points within its neighborhood are shown connected to it.  

###  1. Main function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574544319
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574544319
 ```  
##  III. Display of results 

![avatar]( 47eda4cb81bf49adb396f4c6fe6e7e73.jpeg) 



--------------------------------------------------------------------------------

##  First, the main function 

###  1. K nearest neighbor search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
###  2. Radius search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
###  3. Mixed search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
   SearchHybrid It returns at most the nearest neighbors that are less than a given radius from the query point. This function combines the conditions of KNN search and RNN search. It is called RKNN search in some literature. It has performance advantages in many real-world cases and is widely used in many Open3D functions. 

##  Code implementation 

###  1. K nearest neighbor search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
![avatar]( c78fcd52cfc64a50803f5c5448236f8f.png) 

###  2. Radius search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
![avatar]( d73cbd3e1aae4df98f14c1c94aa8af12.png) 

###  3. Mixed search 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529000
 ```  
![avatar]( 151827b54e00431dbe592b7fb7965ef5.png) 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  The expression of a plane straight line is: suppose there is a point, so the objective function is: find the partial derivatives of:  

  Let the partial derivatives of equations (3) and (4) be 0 to obtain a system of binary linear equations: 

 Remember, so there are: 

 Solve the above equations to obtain  

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574517937
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574517937
 ```  
![avatar]( 5f1f511a415d4c81bc790c60e731f519.png) 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  Let the fitted plane equation be: the constraint condition is: the plane parameters can be obtained. At this time, to make the obtained fitted plane is the best, that is, to minimize the sum of squares of the distance from the point to the plane, that is, to satisfy: where is the distance from any point in the point cloud data to this plane. To make, you can use matrix factorization to get. The derivation process is as follows: the average coordinates of all points are, then: formula (1) is subtracted from formula (4) to obtain: hypothesis matrix: column matrix: then formula (5) is equivalent to: ideally all points are on the plane, formula (6) holds; in practice, some points are outside the plane, and the purpose of fitting is to minimize the sum of the distances from all points in the plane, so the objective function is: The constraints are: 

 If singular value decomposition can be done: then: where: is a column matrix, and: because the diagonal element of is a singular value, assuming that the last diagonal element is the smallest singular value, then if and only if:, formula (10) can obtain the minimum value, that is, formula (7) holds. At this time: the optimal solution of the objective function (7) under the constraint condition (8) is: Therefore, the minimum value of is the minimum eigenvalue of the matrix, and the corresponding eigenvector is a plane parameter, which can be obtained by using the centroid. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574599924
 ```  
##  III. Display of results 

>  Consistent with the calculation results of CloudCompare, the correctness of the algorithm is verified. 

![avatar]( 5452f40653b549d69b6c89b2fa7545be.png) 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  The general expression of the plane equation is as follows: Remember: Substituting equation (3) into equation (2) yields equation (4): For a series of points;, use this point to fit the plane equation, even if:  

  To make the minimum, the two sides of equation (4) should be found to be partial derivative, and the partial derivative should be zero. That is, rewrite it into a matrix form as: solve the equation system (7) to obtain the parameters, and substitute formula (4) to obtain the plane equation. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574582340
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574582340
 ```  


--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

###  1. Overview of the principle 

  When the traditional least squares method is used to fit the plane of point cloud data, the error can be attributed to only one direction. This paper assumes that the error only exists in the axial direction, and the plane equation of point cloud fitting is:  

  When the number of observation points is, taking the coordinates as the observation value, the observation value equation is:  

  The equation (2) is rewritten as an error equation. According to the least squares criterion, the parameter values are obtained by the equal weight adjustment solution of equation (4), and the calculated plane parameter values are substituted into equation (1) to obtain the plane equation of point cloud fitting. 

###  2. References 

>  [1] Bo Huaizhi. Accuracy comparison and analysis of three point cloud data plane fitting methods [J]. Surveying and Mapping and Spatial Geographic Information, 2018, 41 (05): 206-208. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574550893
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574550893
 ```  


--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

  Let the fitted plane equation be: Constraint conditions are: plane parameters can be obtained. At this time, to make the obtained fitted plane is optimal, that is, to minimize the sum of squares of the distance from the point to the plane, that is, to satisfy: In the formula,, is the distance from any point in the point cloud data to this plane. To make, you can use the Lagrange multiplier method to solve the extreme value and get the function:  

  First, find the partial derivative on both sides of formula (2-4), and let the partial derivative be zero, to obtain: let,,, the center of mass be,,, then: then find the partial derivative on both sides of formula (2-4), get  

  The above equations form the eigenvalue equation: In the equation, then, to solve the plane parameters is to solve the eigenvalues and eigenvectors of the matrix. And because it is a third-order real symmetric matrix, the eigenvalue solution formula is: under constraints, get. Therefore, the minimum value is the minimum eigenvalue of the matrix, and the corresponding eigenvector is a plane parameter, which can be obtained by using the centroid. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534277
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534277
 ```  


--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

###  1. Algorithm overview 

  The DeformAsRigidAsPossible function in Open3D, which uses a small number of constraints to deform the triangular mesh, implements the strictest possible algorithm in Sorkine and M. Alexa, As-rigid-as-possible surface modeling, Symposium on Geometry processing, 2007. To optimize the following energy function: where: represents the rotation matrix to be optimized, and represents the vertex positions before and after optimization, respectively, representing the neighborhood set of vertices. The weight represents the cotangent weight (). 

###  2. Main functions 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574574671
 ```  
Energy and smoothed_alpha achieve a smoothed version of the ARAP goal, defined as: penalizing the deviation of adjacent rotation matrices, is the tradeoff parameter of the regularization term, and is the surface area. This smoothing goal can be used in deform_as_rigid_as_possible by using the parameters energy and smoothed_alpha together. 

###  3. References 

>  [1]Sorkine and M. Alexa, As-rigid-as-possible surface modeling, Symposium on Geometry processing, 2007. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574574671
 ```  
##  III. Display of results 

###  1. Original image 

![avatar]( cbbe045b010a4edb82880e85c76f411d.png) 

###  2. Deformation 

![avatar]( 6bfff10294d24257882697e7493e3b57.png) 

##  IV. Experimental data 

Armadillo.pcd Convert the PCD format to ply. 



--------------------------------------------------------------------------------

##  First, the principle of the algorithm 

###  1. Implementation process 

  The minimum spanning tree method is the first and most widely used normal vector adjustment algorithm. The algorithm first determines a seed point, and then traverses the minimum spanning tree (MST) of the point cloud along a relatively flat path, adjusting the normal vector of the points on the path, so that the inner product of the normal vector of the adjacent points is positive. The MST method divides the point cloud model into two parts, the adjusted point set and the unadjusted point set of the normal vector, and then selects the two points with the smallest weight between the and to propagate the normal vector. The direction of the normal vector of the point is determined by the direction of the normal vector of the normal vector to ensure that there is no sudden change in the direction of the normal vector between the two. The selection of weights determines the direction of normal vector propagation. In practice, the algorithm first extracts a sub-point to ensure that the normal vector of the point is correct, and then propagates along the direction with the smallest weight. Every time it propagates to a new point, the normal vector of the new point is modified according to the principle that the normal vector direction does not mutate and the point set sum is updated. The whole traversal process forms a tree containing all points and the sum of the weights of the edges is the smallest. The tree is called MST, so the algorithm is called MST method. Two points in the propagation direction and an edge that constitutes MST. 

###  2. References 

>  Sun Jinhu, Zhou Lishui, An Luling. Optimization algorithm for normal vector adjustment of point cloud model [J]. Chinese Journal of Image and Graphics, 2013, 18 (07): 844-851. 

###  3. Main functions 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596036
 ```  
Use the least cost spanning tree to orient the normal vector. 

###  4. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596036
```cpp
void PointCloud::OrientNormalsConsistentTangentPlane(size_t k) {

    if (!HasNormals()) {

        utility::LogError(

                "[OrientNormalsConsistentTangentPlane] No normals in the "

                "PointCloud. Call EstimateNormals() first.");

    }

    // Create Riemannian graph (Euclidian MST + kNN)

    // Euclidian MST is subgraph of Delaunay triangulation

    std::shared_ptr<TetraMesh> delaunay_mesh;

    std::vector<size_t> pt_map;

    std::tie(delaunay_mesh, pt_map) = TetraMesh::CreateFromPointCloud(*this);

    std::vector<WeightedEdge> delaunay_graph;

    std::unordered_set<size_t> graph_edges;

    auto EdgeIndex = [&](size_t v0, size_t v1) -> size_t {

        return std::min(v0, v1) * points_.size() + std::max(v0, v1);

    };

    auto AddEdgeToDelaunayGraph = [&](size_t v0, size_t v1) {

        v0 = pt_map[v0];

        v1 = pt_map[v1];

        size_t edge = EdgeIndex(v0, v1);

        if (graph_edges.count(edge) == 0) {

            double dist = (points_[v0] - points_[v1]).squaredNorm();

            delaunay_graph.push_back(WeightedEdge(v0, v1, dist));

            graph_edges.insert(edge);

        }

    };

    for (const Eigen::Vector4i &tetra : delaunay_mesh->tetras_) {

        AddEdgeToDelaunayGraph(tetra[0], tetra[1]);

        AddEdgeToDelaunayGraph(tetra[0], tetra[2]);

        AddEdgeToDelaunayGraph(tetra[0], tetra[3]);

        AddEdgeToDelaunayGraph(tetra[1], tetra[2]);

        AddEdgeToDelaunayGraph(tetra[1], tetra[3]);

        AddEdgeToDelaunayGraph(tetra[2], tetra[3]);

    }

    std::vector<WeightedEdge> mst = Kruskal(delaunay_graph, points_.size());

    auto NormalWeight = [&](size_t v0, size_t v1) -> double {

        return 1.0 - std::abs(normals_[v0].dot(normals_[v1]));

    };

    for (auto &edge : mst) {

        edge.weight_ = NormalWeight(edge.v0_, edge.v1_);

    }

    // Add k nearest neighbors to Riemannian graph

    KDTreeFlann kdtree(*this);

    for (size_t v0 = 0; v0 < points_.size(); ++v0) {

        std::vector<int> neighbors;

        std::vector<double> dists2;

        kdtree.SearchKNN(points_[v0], int(k), neighbors, dists2);

        for (size_t vidx1 = 0; vidx1 < neighbors.size(); ++vidx1) {

            size_t v1 = size_t(neighbors[vidx1]);

            if (v0 == v1) {

                continue;

            }

            size_t edge = EdgeIndex(v0, v1);

            if (graph_edges.count(edge) == 0) {

                double weight = NormalWeight(v0, v1);

                mst.push_back(WeightedEdge(v0, v1, weight));

                graph_edges.insert(edge);

            }

        }

    }

    // extract MST from Riemannian graph

    mst = Kruskal(mst, points_.size());

    // convert list of edges to graph

    std::vector<std::unordered_set<size_t>> mst_graph(points_.size());

    for (const auto &edge : mst) {

        size_t v0 = edge.v0_;

        size_t v1 = edge.v1_;

        mst_graph[v0].insert(v1);

        mst_graph[v1].insert(v0);

    }

    // find start node for tree traversal

    // init with node that maximizes z

    double max_z = std::numeric_limits<double>::lowest();

    size_t v0 = 0;

    for (size_t vidx = 0; vidx < points_.size(); ++vidx) {

        const Eigen::Vector3d &v = points_[vidx];

        if (v(2) > max_z) {

            max_z = v(2);

            v0 = vidx;

        }

    }

    // traverse MST and orient normals consistently

    std::queue<size_t> traversal_queue;

    std::vector<bool> visited(points_.size(), false);

    traversal_queue.push(v0);

    auto TestAndOrientNormal = [&] (const Own:: Vector3d & n0,

                                   Own:: Vector3d & n1) {

        if (n0.dot(n1) < 0) {

            n1 *= -1;

        }

    };

    TestAndOrientNormal(Eigen::Vector3d(0, 0, 1), normals_[v0]);

    while (!traversal_queue.empty()) {

        v0 = traversal_queue.front();

        traversal_queue.pop();

        visited[v0] = true;

        for (size_t v1 : mst_graph[v0]) {

            if (!visited[v1]) {

                traversal_queue.push(v1);

                TestAndNormal Orient (normal_[v0], normal_[v1]);

            }

        }

    }

}

 ```  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596036
 ```python  
#include <iostream>

#include <Open3D/Open3D.h>

using namespace std;

int main(int argc, char* argv[])

{

	//------------------------- load point cloud data -----------------------------

	auto cloud = std::make_shared<open3d::geometry::PointCloud>();

	if (open3d::io::ReadPointCloud("E://data//bunny.pcd", *cloud) == 0)

	{

		Ope n 3d :: utility :: Log War n i n g ("Point cloud reading failed!!!\ n\ n");

		return -1;

	}

	Cout < < "Read from point cloud data" < < cloud- > points_ size () << " points "< < endl;

	//------------------------ compute the normal vector -------------------------- of the point cloud

	Open 3d :: utility :: LogIn fo ("Compute point cloud normal vector");

	//Compute normal for every point parameter[radius: searching radius, max_nn: maximum nearest neighbor]

	cloud->EstimateNormals(open3d::geometry::KDTreeSearchParamHybrid(0.1, 30));

	//----------------------- minimum cost spanning tree oriented --------------------------

    cloud->OrientNormalsConsistentTangentPlane (10);

	if (cloud->HasNormals())

	{

		Cloud- > NormalizeNormals (); // normalize normal vector to 1

	}

	Open 3d :: utility :: LogIn fo ("print the normal vector of point 0");

	std::cout << cloud->normals_[0] << std::endl;

	//------------------------- visualize normal vector ------------------------------

	bool point_show_normal = true;

	bool mesh_show_wireframe = false;

	bool mesh_show_back_face = true;

	open3d::visualization::DrawGeometries({ cloud }, "PointCloud", 1200, 800,

		point_show_normal, mesh_show_wireframe, mesh_show_back_face);

	return 0;

}

 ```  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596036


--------------------------------------------------------------------------------

##  I. Overview 

  Both mean filtering and Laplace filtering make the triangular mesh shrink. The Taubin filter uses two Laplace filters with different parameters to prevent mesh shrinkage. The implementation interface of this filter is: FilterSmoothTaubin. 

###  1. Main function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558278
 ```  
###  2. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558278
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558278
 ```  
##  III. Display of results 

###  1. The original model 

![avatar]( 33485d22c39443ce82f196ffc01d6681.png) 

###  2. The filtered model 

![avatar]( 0e2e873d6b4b4d7287d11fb7156f1b11.png) 



--------------------------------------------------------------------------------

##  I. Overview 

###  1. Algorithm principle 

  The Laplace operator is an important mesh filter and is defined as follows:  

  Here is the filter strength, which is a normalized weight related to the distance from neighbors. 

###  2. Main functions 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534962
 ```  
###  3. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534962
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534962
 ```  
##  III. Display of results 

![avatar]( 7a6ea5f39ebd4688b402351e3608b07c.png) 



--------------------------------------------------------------------------------

##  I. Overview 

###  1. Algorithm principle 

  Open3d includes many mesh filtering algorithms, the simplest of which is the mean filter, which can be used to de-noise the mesh. The value of a vertex is given by the average of adjacent vertices. The formula is as follows:  

###  2. Main functions 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577433
 ```  
###  3. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577433
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577433
 ```  
##  III. Display of results 

![avatar]( 651354430b124a60adb19d4f1a932066.png) 



--------------------------------------------------------------------------------

##  I. Overview 

  The range of colors in Open3D is [0.0, 1.0]. The function rand () in C++ can be used to generate random numbers, and its return value is an integer. To generate floating-point numbers between 0.0 and 1.0, it must be converted. First generate a random number of 0-N, and then divide it by N + 1 converted to floating-point numbers to get the random number generator we want. Where N can adjust the range of precision we want, when N = 99, keep two decimal places. Model color function: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745514
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745514
 ```  
##  III. Display of results 

![avatar]( f6c0c308befd452abd2d38394776b73f.png) 



--------------------------------------------------------------------------------

##  I. Overview of algorithms 

  Model refinement involves dividing each triangle into smaller triangles. The simplest way is to calculate the midpoint of each side of the triangle and divide it into four smaller triangles. This is achieved through the SubdivideLoop function. The 3D surface and area remain the same, but the number of vertices and triangles increases. number_of_iterations parameter defines the number of refinements. 

###  1. Main function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957459629
 ```  
This function converts a triangle into four triangles that cover the same surface. 

###  2. References 

>  [1] Cf. Charles T. Loop, “Smooth subdivision surfaces based on triangles”,1987. 

###  3. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957459629
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957459629
 ```  
##  III. Display of results 

![avatar]( 20201203212344301.png) 



--------------------------------------------------------------------------------

##  I. Overview of algorithms 

  Triangles are refined using a simple midpoint algorithm. Each iteration subdivides the triangle into four triangles, with the subdivided vertices located at the midpoint of the original triangle's edge. number_of_iterations parameter defines the number of refinements. 

###  1. Main function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513176
 ```  
This function transforms the triangle into four triangles covering the same surface, with the new quadrilateral vertices located at the midpoint of the sides of the original triangle. 

###  2. Algorithm source code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513176
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513176
 ```  
##  III. Display of results 

![avatar]( 16c896c163444825ac17eb98663f55d5.png) 

 1. The original model 2. The processed model  



--------------------------------------------------------------------------------

##  First, model sharpening 

###  1. Overview 

  The output value () of the algorithm is the sum of the input value () plus the filter enhancement factor multiplied by the input value minus adjacent values.  

###  2. Main functions 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957453397
 ```  
##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957453397
 ```  
##  III. Display of results 

###  1. The original model 

![avatar]( 1bf1b2ac1e0645d589c6fb87438c4074.png) 

###  2. Sharpening 

![avatar]( 6c8ee72ca86844b89d6cf6f34abcb396.png) 



--------------------------------------------------------------------------------

##  First, grid extraction 

  Another way to simplify meshes is to perform step-by-step mesh extraction. Select a triangle removal that minimizes the error metric. Repeat this process until the specified number of triangles is met. Open3d implements SimplifyQuadricDecimation interface to minimize the error square (distance from adjacent planes), and the parameter target_number_of_triangles defines the number of facets to stop extracting. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574551428
 ```  
Simplify the grid function using quadratic error metric extraction. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574551428
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574551428
 ```  
![avatar]( 1658c0776fc348a682d49a7050b15756.png) 

![avatar]( 32a72b254c6e407e8b0fc99aca84c90a.png) 



--------------------------------------------------------------------------------

