---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277022"
---
# <span data-ttu-id="07e89-101">Az. ServiceFabric modülü</span><span class="sxs-lookup"><span data-stu-id="07e89-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="07e89-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="07e89-102">Description</span></span>
<span data-ttu-id="07e89-103">Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="07e89-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="07e89-104">Az. ServiceFabric cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="07e89-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="07e89-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="07e89-106">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="07e89-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="07e89-108">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="07e89-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="07e89-110">Kümeye sertifika ortak adı veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="07e89-111">Bu işlem, sertifikayı istemci kimlik doğrulama amaçları için kümenin içine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="07e89-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="07e89-112">Add-Azservicefabricmanagednodetypevmexgeri</span><span class="sxs-lookup"><span data-stu-id="07e89-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="07e89-113">Düğüm türüne VM Uzantısı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="07e89-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="07e89-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="07e89-115">Düğüm türüne sertifika parolası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="07e89-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="07e89-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="07e89-117">Kümedeki belirli bir düğüme düğüm ekleme.</span><span class="sxs-lookup"><span data-stu-id="07e89-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="07e89-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="07e89-119">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="07e89-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07e89-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="07e89-121">Hizmet dokusu uygulama ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="07e89-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07e89-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="07e89-123">Hizmet dokusu uygulama türü ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="07e89-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07e89-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="07e89-125">Hizmet dokusu uygulama türü sürüm bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="07e89-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="07e89-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="07e89-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="07e89-127">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="07e89-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="07e89-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="07e89-129">Yönetilen küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="07e89-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="07e89-131">Yönetilen düğüm türü kaynak ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="07e89-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="07e89-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="07e89-133">Belirtilen uygulama ve kümenin altındaki hizmet Fabric hizmeti ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="07e89-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="07e89-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07e89-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="07e89-135">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="07e89-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07e89-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="07e89-137">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulama türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="07e89-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07e89-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="07e89-139">Belirtilen kaynak grubu ve küme altında yeni uygulama türü sürümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="07e89-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="07e89-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="07e89-141">Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="07e89-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="07e89-142">Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="07e89-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="07e89-143">Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07e89-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="07e89-144">Yeni-Azhizmetifabricmanagedcluster</span><span class="sxs-lookup"><span data-stu-id="07e89-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="07e89-145">Yeni yönetilen küme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="07e89-146">Yeni-Azhizmetifabricmanagednodetype</span><span class="sxs-lookup"><span data-stu-id="07e89-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="07e89-147">Yeni düğüm türü kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-147">Create new node type resource.</span></span>

### [<span data-ttu-id="07e89-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="07e89-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="07e89-149">Belirtilen uygulama ve küme altında yeni hizmet yapısı hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07e89-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="07e89-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07e89-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="07e89-151">Kümeden bir uygulamayı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-151">Remove an application from the cluster.</span></span> <span data-ttu-id="07e89-152">Bu işlem, uygulamanın altındaki tüm hizmetleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07e89-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="07e89-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="07e89-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="07e89-154">Service Fabric 'ı kümeden bir uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="07e89-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="07e89-155">Bu, bu kaynağın altındaki tüm tür sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07e89-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="07e89-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="07e89-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="07e89-157">Hizmet yapısı 'nı kümeden uygulama türü sürümü.</span><span class="sxs-lookup"><span data-stu-id="07e89-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="07e89-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="07e89-159">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="07e89-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="07e89-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="07e89-161">Küme güvenliği için kullanılan küme sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="07e89-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="07e89-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="07e89-163">Küme kaynağını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="07e89-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="07e89-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="07e89-165">Parmak izi veya ortak ada göre remvoe istemci sertifikası.</span><span class="sxs-lookup"><span data-stu-id="07e89-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="07e89-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="07e89-167">Düğüm türünü veya düğüm türü içindeki belirli düğümleri kaldırın.</span><span class="sxs-lookup"><span data-stu-id="07e89-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="07e89-168">Remove-Azservicefabricmanagednodetypevmexgeri</span><span class="sxs-lookup"><span data-stu-id="07e89-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="07e89-169">Düğüm türünden VM uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="07e89-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="07e89-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="07e89-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="07e89-171">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="07e89-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="07e89-173">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="07e89-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="07e89-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="07e89-175">Kümeden bir hizmeti kaldırma.</span><span class="sxs-lookup"><span data-stu-id="07e89-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="07e89-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="07e89-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="07e89-177">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="07e89-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="07e89-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="07e89-179">Düğüm türünden belirli düğümleri yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="07e89-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="07e89-180">Set-Azhizmetifabricmanagedcluster</span><span class="sxs-lookup"><span data-stu-id="07e89-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="07e89-181">Küme kaynağı özelliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="07e89-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="07e89-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="07e89-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="07e89-183">Düğüm türü kaynak özelliklerini ayarlar ya da-Reimage parametresi</span><span class="sxs-lookup"><span data-stu-id="07e89-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="07e89-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="07e89-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="07e89-185">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="07e89-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="07e89-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="07e89-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="07e89-187">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="07e89-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="07e89-188">Güncelleştirme-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="07e89-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="07e89-189">Hizmet dokusu uygulamasını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="07e89-189">Update a service fabric application.</span></span> <span data-ttu-id="07e89-190">Bu, uygulama parametrelerini güncellemesine ve/veya uygulama yükseltmesini tetikleyecek uygulama türü sürümünü yükseltmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="07e89-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="07e89-191">Güncelleştirme-Azservicefabricdayanıklılığı</span><span class="sxs-lookup"><span data-stu-id="07e89-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="07e89-192">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="07e89-193">Update-Azservicefabricgüvenirlik</span><span class="sxs-lookup"><span data-stu-id="07e89-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="07e89-194">Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="07e89-194">Update the reliability tier of the primary node type in a cluster.</span></span>

