---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935199"
---
# <span data-ttu-id="c670f-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="c670f-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="c670f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c670f-102">SYNOPSIS</span></span>
<span data-ttu-id="c670f-103">Ada göre bir güncelleştirme konumu alın.</span><span class="sxs-lookup"><span data-stu-id="c670f-103">Get an update location based on name.</span></span>

## <span data-ttu-id="c670f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c670f-104">SYNTAX</span></span>

### <span data-ttu-id="c670f-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c670f-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c670f-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c670f-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c670f-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="c670f-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c670f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c670f-108">DESCRIPTION</span></span>
<span data-ttu-id="c670f-109">Ada göre bir güncelleştirme konumu alın.</span><span class="sxs-lookup"><span data-stu-id="c670f-109">Get an update location based on name.</span></span>

## <span data-ttu-id="c670f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c670f-110">EXAMPLES</span></span>

### <span data-ttu-id="c670f-111">Örnek 1: tüm güncelleştirme konumlarını alma</span><span class="sxs-lookup"><span data-stu-id="c670f-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="c670f-112">Parametresiz, bu komut</span><span class="sxs-lookup"><span data-stu-id="c670f-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="c670f-113">Örnek 2: tüm güncelleştirmeleri ada göre alma</span><span class="sxs-lookup"><span data-stu-id="c670f-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="c670f-114">Belirtilen ad parametresiyle eşleşen tüm güncelleştirme konumlarını alacak</span><span class="sxs-lookup"><span data-stu-id="c670f-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="c670f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c670f-115">PARAMETERS</span></span>

### <span data-ttu-id="c670f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c670f-116">-DefaultProfile</span></span>
<span data-ttu-id="c670f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c670f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c670f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c670f-118">-InputObject</span></span>
<span data-ttu-id="c670f-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c670f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c670f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c670f-120">-Name</span></span>
<span data-ttu-id="c670f-121">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="c670f-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c670f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c670f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c670f-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c670f-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c670f-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c670f-124">-SubscriptionId</span></span>
<span data-ttu-id="c670f-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c670f-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c670f-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c670f-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c670f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c670f-127">CommonParameters</span></span>
<span data-ttu-id="c670f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c670f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c670f-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c670f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c670f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c670f-130">INPUTS</span></span>

### <span data-ttu-id="c670f-131">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. ıupdateadminıdentity</span><span class="sxs-lookup"><span data-stu-id="c670f-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="c670f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c670f-132">OUTPUTS</span></span>

### <span data-ttu-id="c670f-133">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. Api20160501. ıupdatelocation</span><span class="sxs-lookup"><span data-stu-id="c670f-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="c670f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c670f-134">NOTES</span></span>

<span data-ttu-id="c670f-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c670f-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c670f-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c670f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c670f-137">INPUTOBJECT <IUpdateAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c670f-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c670f-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c670f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c670f-139">`[ResourceGroupName <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c670f-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="c670f-140">`[RunName <String>]`: Güncelleştirme çalıştırması tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c670f-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="c670f-141">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c670f-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="c670f-142">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c670f-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c670f-143">`[UpdateLocation <String>]`: Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="c670f-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="c670f-144">`[UpdateName <String>]`: Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="c670f-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="c670f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c670f-145">RELATED LINKS</span></span>

