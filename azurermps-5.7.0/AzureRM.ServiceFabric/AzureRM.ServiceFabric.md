---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570637"
---
# <span data-ttu-id="27051-101">AzureRM. ServiceFabric modülü</span><span class="sxs-lookup"><span data-stu-id="27051-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="27051-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="27051-102">Description</span></span>
<span data-ttu-id="27051-103">Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="27051-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="27051-104">AzureRM. ServiceFabric cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="27051-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="27051-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="27051-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="27051-106">Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="27051-107">Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="27051-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="27051-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="27051-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="27051-109">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="27051-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="27051-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="27051-111">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="27051-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="27051-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="27051-113">Kümedeki belirli bir düğüme düğüm ekleme.</span><span class="sxs-lookup"><span data-stu-id="27051-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="27051-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="27051-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="27051-115">Var olan kümeye yeni bir düğüm türü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="27051-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="27051-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="27051-117">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="27051-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="27051-118">Yeni-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="27051-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="27051-119">Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="27051-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="27051-120">Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="27051-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="27051-121">Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27051-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="27051-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="27051-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="27051-123">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="27051-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="27051-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="27051-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="27051-125">Küme güvenliği için kullanılan küme sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="27051-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="27051-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="27051-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="27051-127">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="27051-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="27051-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="27051-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="27051-129">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="27051-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="27051-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="27051-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="27051-131">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="27051-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="27051-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="27051-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="27051-133">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="27051-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="27051-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="27051-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="27051-135">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="27051-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="27051-136">Güncelleştirme-Azurermservicefabricdayanıklılığı</span><span class="sxs-lookup"><span data-stu-id="27051-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="27051-137">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="27051-138">Güncelleştirme-Azurermservicefabricgüvenirlik</span><span class="sxs-lookup"><span data-stu-id="27051-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="27051-139">Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="27051-139">Update the reliability tier of the primary node type in a cluster.</span></span>

