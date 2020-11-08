---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107441"
---
# <span data-ttu-id="f553b-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="f553b-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="f553b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f553b-102">SYNOPSIS</span></span>
<span data-ttu-id="f553b-103">Özel bulutta ada göre küme alma</span><span class="sxs-lookup"><span data-stu-id="f553b-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f553b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f553b-104">SYNTAX</span></span>

### <span data-ttu-id="f553b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f553b-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f553b-106">Al</span><span class="sxs-lookup"><span data-stu-id="f553b-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f553b-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f553b-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f553b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f553b-108">DESCRIPTION</span></span>
<span data-ttu-id="f553b-109">Özel bulutta ada göre küme alma</span><span class="sxs-lookup"><span data-stu-id="f553b-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="f553b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f553b-110">EXAMPLES</span></span>

### <span data-ttu-id="f553b-111">Örnek 1: küme alma</span><span class="sxs-lookup"><span data-stu-id="f553b-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f553b-112">Küme al</span><span class="sxs-lookup"><span data-stu-id="f553b-112">Get cluster</span></span>

### <span data-ttu-id="f553b-113">Örnek 2: liste kümeleri</span><span class="sxs-lookup"><span data-stu-id="f553b-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f553b-114">Liste kümeleri</span><span class="sxs-lookup"><span data-stu-id="f553b-114">List clusters</span></span>

## <span data-ttu-id="f553b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f553b-115">PARAMETERS</span></span>

### <span data-ttu-id="f553b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f553b-116">-DefaultProfile</span></span>
<span data-ttu-id="f553b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f553b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f553b-118">-InputObject</span></span>
<span data-ttu-id="f553b-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f553b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f553b-120">-Name</span></span>
<span data-ttu-id="f553b-121">Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="f553b-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f553b-122">-PrivateCloudName</span></span>
<span data-ttu-id="f553b-123">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="f553b-123">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f553b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f553b-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f553b-125">The name of the resource group.</span></span>
<span data-ttu-id="f553b-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="f553b-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f553b-127">-SubscriptionId</span></span>
<span data-ttu-id="f553b-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f553b-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f553b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f553b-129">CommonParameters</span></span>
<span data-ttu-id="f553b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f553b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f553b-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f553b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f553b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f553b-132">INPUTS</span></span>

### <span data-ttu-id="f553b-133">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="f553b-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f553b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f553b-134">OUTPUTS</span></span>

### <span data-ttu-id="f553b-135">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıluster</span><span class="sxs-lookup"><span data-stu-id="f553b-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="f553b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f553b-136">NOTES</span></span>

<span data-ttu-id="f553b-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f553b-137">ALIASES</span></span>

<span data-ttu-id="f553b-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f553b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f553b-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f553b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f553b-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f553b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f553b-141">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f553b-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f553b-142">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="f553b-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f553b-143">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="f553b-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f553b-144">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="f553b-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f553b-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f553b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f553b-146">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="f553b-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f553b-147">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="f553b-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f553b-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f553b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f553b-149">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="f553b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f553b-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f553b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f553b-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f553b-151">RELATED LINKS</span></span>

