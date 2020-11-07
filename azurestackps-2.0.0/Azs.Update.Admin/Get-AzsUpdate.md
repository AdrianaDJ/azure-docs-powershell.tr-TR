---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935202"
---
# <span data-ttu-id="c66c7-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="c66c7-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="c66c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c66c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c66c7-103">Güncelleştirme konumunda belirli bir güncelleştirmeyi edinin.</span><span class="sxs-lookup"><span data-stu-id="c66c7-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="c66c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c66c7-104">SYNTAX</span></span>

### <span data-ttu-id="c66c7-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c66c7-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c66c7-106">Al</span><span class="sxs-lookup"><span data-stu-id="c66c7-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c66c7-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c66c7-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c66c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c66c7-108">DESCRIPTION</span></span>
<span data-ttu-id="c66c7-109">Güncelleştirme konumunda belirli bir güncelleştirmeyi edinin.</span><span class="sxs-lookup"><span data-stu-id="c66c7-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="c66c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c66c7-110">EXAMPLES</span></span>

### <span data-ttu-id="c66c7-111">Örnek 1: tüm güncelleştirmeleri alma</span><span class="sxs-lookup"><span data-stu-id="c66c7-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="c66c7-112">Herhangi bir parametre olmadan Get-AzsUpdate damgasının keşfedeyapabileceği tüm güncelleştirmeleri listeler</span><span class="sxs-lookup"><span data-stu-id="c66c7-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="c66c7-113">Örnek 2: ada göre güncelleştirme alma</span><span class="sxs-lookup"><span data-stu-id="c66c7-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="c66c7-114">Belirtilen ada karşılık gelen tüm güncelleştirmeleri alacak</span><span class="sxs-lookup"><span data-stu-id="c66c7-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="c66c7-115">Örnek 3: konuma göre tüm güncelleştirmeleri alma</span><span class="sxs-lookup"><span data-stu-id="c66c7-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="c66c7-116">Belirtilen konumdaki tüm güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="c66c7-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="c66c7-117">Şu anda yalnızca bir konum destekleniyor, bu nedenle bu değer yalnızca Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="c66c7-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="c66c7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c66c7-118">PARAMETERS</span></span>

### <span data-ttu-id="c66c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66c7-119">-DefaultProfile</span></span>
<span data-ttu-id="c66c7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c66c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c66c7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c66c7-121">-InputObject</span></span>
<span data-ttu-id="c66c7-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c66c7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c66c7-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="c66c7-123">-Location</span></span>
<span data-ttu-id="c66c7-124">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c66c7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="c66c7-125">-Name</span></span>
<span data-ttu-id="c66c7-126">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-126">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c66c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c66c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="c66c7-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-128">Resource group name.</span></span>

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

### <span data-ttu-id="c66c7-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c66c7-129">-SubscriptionId</span></span>
<span data-ttu-id="c66c7-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c66c7-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c66c7-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c66c7-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c66c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66c7-132">CommonParameters</span></span>
<span data-ttu-id="c66c7-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c66c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66c7-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c66c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66c7-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c66c7-135">INPUTS</span></span>

### <span data-ttu-id="c66c7-136">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. ıupdateadminıdentity</span><span class="sxs-lookup"><span data-stu-id="c66c7-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="c66c7-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c66c7-137">OUTPUTS</span></span>

### <span data-ttu-id="c66c7-138">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. Api20160501. ıupdate</span><span class="sxs-lookup"><span data-stu-id="c66c7-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="c66c7-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c66c7-139">NOTES</span></span>

<span data-ttu-id="c66c7-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c66c7-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c66c7-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c66c7-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c66c7-142">INPUTOBJECT <IUpdateAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c66c7-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c66c7-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c66c7-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c66c7-144">`[ResourceGroupName <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="c66c7-145">`[RunName <String>]`: Güncelleştirme çalıştırması tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="c66c7-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c66c7-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="c66c7-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c66c7-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c66c7-148">`[UpdateLocation <String>]`: Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="c66c7-149">`[UpdateName <String>]`: Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="c66c7-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="c66c7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c66c7-150">RELATED LINKS</span></span>

