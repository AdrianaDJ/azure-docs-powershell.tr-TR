---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570909"
---
# <span data-ttu-id="5d3dc-101">AzureRM. ServiceFabric modülü</span><span class="sxs-lookup"><span data-stu-id="5d3dc-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="5d3dc-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d3dc-102">Description</span></span>
<span data-ttu-id="5d3dc-103">Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="5d3dc-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="5d3dc-104">AzureRM. ServiceFabric cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5d3dc-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="5d3dc-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3dc-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="5d3dc-106">Uygulama sertifikası olarak kullanılacak bir sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="5d3dc-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3dc-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="5d3dc-108">İstemci kimlik doğrulaması için küme ayarlarına ortak ad veya parmak izi ekleme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="5d3dc-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3dc-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="5d3dc-110">Var olan sertifikanın üzerine gitmek için kümeye ikincil küme sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="5d3dc-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5d3dc-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="5d3dc-112">Belirli bir düğüm türüne düğüm/VM ekleme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="5d3dc-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5d3dc-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="5d3dc-114">Var olan bir kümeye düğüm türü/VM 'Ler ekleme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="5d3dc-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5d3dc-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="5d3dc-116">Küme kaynağının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="5d3dc-117">Yeni-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5d3dc-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="5d3dc-118">Yeni bir ServiceFabric kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d3dc-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="5d3dc-119">Bu komutun çeşitli senaryoları kapsayacak birçok yüklemesi vardır</span><span class="sxs-lookup"><span data-stu-id="5d3dc-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="5d3dc-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3dc-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="5d3dc-121">Kümeye erişmek için kullanılan istemci sertifikasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="5d3dc-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3dc-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="5d3dc-123">Küme sertifikasının küme güvenliği için kullanılmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="5d3dc-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5d3dc-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="5d3dc-125">Belirli düğüm türünden düğümleri kümeden kaldırma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="5d3dc-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5d3dc-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="5d3dc-127">Kümeden düğüm türünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="5d3dc-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5d3dc-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="5d3dc-129">Kümeden bir veya daha fazla ServiceFabric ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5d3dc-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="5d3dc-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5d3dc-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="5d3dc-131">Kümeye bir veya daha fazla ServiceFabric ayarı ekleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="5d3dc-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="5d3dc-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="5d3dc-133">Kümenin ServiceFabric yükseltme türünü değiştirme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="5d3dc-134">Güncelleştirme-Azurermservicefabricdayanıklılığı</span><span class="sxs-lookup"><span data-stu-id="5d3dc-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="5d3dc-135">Kümenin dayanıklılık katmanını değiştirme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="5d3dc-136">Güncelleştirme-Azurermservicefabricgüvenirlik</span><span class="sxs-lookup"><span data-stu-id="5d3dc-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="5d3dc-137">Kümenin güvenilirlik katmanını değiştirme</span><span class="sxs-lookup"><span data-stu-id="5d3dc-137">Change the reliability tier of a cluster</span></span>
