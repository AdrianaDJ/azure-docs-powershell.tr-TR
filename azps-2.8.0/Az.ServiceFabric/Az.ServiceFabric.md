---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93751082"
---
# <span data-ttu-id="4078e-101">Az. ServiceFabric modülü</span><span class="sxs-lookup"><span data-stu-id="4078e-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="4078e-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="4078e-102">Description</span></span>
<span data-ttu-id="4078e-103">Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4078e-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="4078e-104">Az. ServiceFabric cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4078e-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="4078e-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4078e-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="4078e-106">Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="4078e-107">Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4078e-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="4078e-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4078e-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="4078e-109">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="4078e-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4078e-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="4078e-111">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="4078e-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4078e-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="4078e-113">Kümedeki belirli bir düğüme düğüm ekleme.</span><span class="sxs-lookup"><span data-stu-id="4078e-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="4078e-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="4078e-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="4078e-115">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="4078e-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4078e-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="4078e-117">Hizmet dokusu uygulama ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4078e-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="4078e-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4078e-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="4078e-119">Hizmet dokusu uygulama türü ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4078e-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="4078e-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4078e-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="4078e-121">Hizmet dokusu uygulama türü sürüm bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="4078e-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="4078e-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4078e-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="4078e-123">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4078e-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="4078e-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4078e-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="4078e-125">Belirtilen uygulama ve kümenin altındaki hizmet Fabric hizmeti ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4078e-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="4078e-126">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4078e-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="4078e-127">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4078e-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="4078e-128">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4078e-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="4078e-129">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulama türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4078e-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="4078e-130">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4078e-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="4078e-131">Belirtilen kaynak grubu ve küme altında yeni uygulama türü sürümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4078e-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="4078e-132">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4078e-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="4078e-133">Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="4078e-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="4078e-134">Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4078e-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="4078e-135">Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4078e-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="4078e-136">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4078e-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="4078e-137">Belirtilen uygulama ve küme altında yeni hizmet yapısı hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4078e-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="4078e-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4078e-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="4078e-139">Kümeden bir uygulamayı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4078e-139">Remove an application from the cluster.</span></span> <span data-ttu-id="4078e-140">Bu işlem, uygulamanın altındaki tüm hizmetleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4078e-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="4078e-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4078e-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="4078e-142">Service Fabric 'ı kümeden bir uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="4078e-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="4078e-143">Bu, bu kaynağın altındaki tüm tür sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4078e-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="4078e-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4078e-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="4078e-145">Hizmet yapısı 'nı kümeden uygulama türü sürümü.</span><span class="sxs-lookup"><span data-stu-id="4078e-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="4078e-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4078e-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="4078e-147">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="4078e-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="4078e-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4078e-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="4078e-149">Küme güvenliği için kullanılan küme sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4078e-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="4078e-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4078e-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="4078e-151">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4078e-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="4078e-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="4078e-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="4078e-153">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4078e-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="4078e-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4078e-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="4078e-155">Kümeden bir hizmeti kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4078e-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="4078e-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="4078e-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="4078e-157">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="4078e-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="4078e-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="4078e-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="4078e-159">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="4078e-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="4078e-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="4078e-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="4078e-161">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4078e-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="4078e-162">Güncelleştirme-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4078e-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="4078e-163">Hizmet dokusu uygulamasını güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4078e-163">Update a service fabric application.</span></span> <span data-ttu-id="4078e-164">Bu, uygulama parametrelerini güncellemesine ve/veya uygulama yükseltmesini tetikleyecek uygulama türü sürümünü yükseltmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4078e-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="4078e-165">Güncelleştirme-Azservicefabricdayanıklılığı</span><span class="sxs-lookup"><span data-stu-id="4078e-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="4078e-166">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="4078e-167">Update-Azservicefabricgüvenirlik</span><span class="sxs-lookup"><span data-stu-id="4078e-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="4078e-168">Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4078e-168">Update the reliability tier of the primary node type in a cluster.</span></span>

