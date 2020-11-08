---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267490"
---
# <span data-ttu-id="4e782-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="4e782-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="4e782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e782-102">SYNOPSIS</span></span>
<span data-ttu-id="4e782-103">Özel bulutta ada göre bir ExpressRoute devresi yetkilendirmesi alma</span><span class="sxs-lookup"><span data-stu-id="4e782-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="4e782-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e782-104">SYNTAX</span></span>

### <span data-ttu-id="4e782-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4e782-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e782-106">Al</span><span class="sxs-lookup"><span data-stu-id="4e782-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e782-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4e782-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4e782-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e782-108">DESCRIPTION</span></span>
<span data-ttu-id="4e782-109">Özel bulutta ada göre bir ExpressRoute devresi yetkilendirmesi alma</span><span class="sxs-lookup"><span data-stu-id="4e782-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="4e782-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e782-110">EXAMPLES</span></span>

### <span data-ttu-id="4e782-111">Örnek 1: yetkilendirmeyi alma</span><span class="sxs-lookup"><span data-stu-id="4e782-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="4e782-112">Bu cmdlet `azps-test-auth` özel bulut altında yetkilendirmeyi alır `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="4e782-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="4e782-113">Örnek 2: kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="4e782-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="4e782-114">Bu cmdlet, `azps-test-auth` özel bulut altında yetkilendirmeyi listeler `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="4e782-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="4e782-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e782-115">PARAMETERS</span></span>

### <span data-ttu-id="4e782-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e782-116">-DefaultProfile</span></span>
<span data-ttu-id="4e782-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e782-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e782-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e782-118">-InputObject</span></span>
<span data-ttu-id="4e782-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4e782-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e782-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e782-120">-Name</span></span>
<span data-ttu-id="4e782-121">Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="4e782-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e782-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="4e782-122">-PrivateCloudName</span></span>
<span data-ttu-id="4e782-123">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="4e782-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="4e782-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e782-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e782-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4e782-125">The name of the resource group.</span></span>
<span data-ttu-id="4e782-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4e782-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4e782-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4e782-127">-SubscriptionId</span></span>
<span data-ttu-id="4e782-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4e782-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4e782-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e782-129">CommonParameters</span></span>
<span data-ttu-id="4e782-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e782-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e782-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4e782-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e782-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e782-132">INPUTS</span></span>

### <span data-ttu-id="4e782-133">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="4e782-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4e782-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e782-134">OUTPUTS</span></span>

### <span data-ttu-id="4e782-135">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıexpressrouteauthorization</span><span class="sxs-lookup"><span data-stu-id="4e782-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="4e782-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e782-136">NOTES</span></span>

<span data-ttu-id="4e782-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4e782-137">ALIASES</span></span>

<span data-ttu-id="4e782-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4e782-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e782-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4e782-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e782-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e782-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e782-141">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4e782-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e782-142">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="4e782-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4e782-143">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="4e782-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4e782-144">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="4e782-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4e782-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4e782-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e782-146">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="4e782-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4e782-147">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="4e782-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4e782-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4e782-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4e782-149">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4e782-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="4e782-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4e782-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4e782-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e782-151">RELATED LINKS</span></span>

