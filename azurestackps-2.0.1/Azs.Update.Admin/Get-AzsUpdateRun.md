---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 1a5cfb9f9bc7edb436d37847fc117565c3b71221
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105323"
---
# <span data-ttu-id="57a2a-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="57a2a-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="57a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="57a2a-103">KIMLIK kullanarak güncelleştirme çalıştırması örneği edinin.</span><span class="sxs-lookup"><span data-stu-id="57a2a-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="57a2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57a2a-104">SYNTAX</span></span>

### <span data-ttu-id="57a2a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57a2a-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57a2a-106">Al</span><span class="sxs-lookup"><span data-stu-id="57a2a-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57a2a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="57a2a-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57a2a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="57a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="57a2a-109">KIMLIK kullanarak güncelleştirme çalıştırması örneği edinin.</span><span class="sxs-lookup"><span data-stu-id="57a2a-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="57a2a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57a2a-110">EXAMPLES</span></span>

### <span data-ttu-id="57a2a-111">Örnek 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="57a2a-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="57a2a-112">UpdateName değeri belirtilmemişse Get-UpdateRun her zaman giriş sorar.</span><span class="sxs-lookup"><span data-stu-id="57a2a-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="57a2a-113">Bu, bir kez sağlandığında, başarısız</span><span class="sxs-lookup"><span data-stu-id="57a2a-113">Once provided, it will output all instances of UpdateRun that were Failed or Successfull</span></span>

### <span data-ttu-id="57a2a-114">Örnek 2 Get-AzsUpdateRun: Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="57a2a-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="57a2a-115">Belirli bir güncelleştirmeyle ilişkilendirilmiş tüm Updaterlerkonları alacak</span><span class="sxs-lookup"><span data-stu-id="57a2a-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="57a2a-116">Örnek 2: ada göre Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="57a2a-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="57a2a-117">Belirli bir güncelleştirmeyle ve belirli bir adla ilişkili tüm Updaterlerkonları alacak</span><span class="sxs-lookup"><span data-stu-id="57a2a-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="57a2a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57a2a-118">PARAMETERS</span></span>

### <span data-ttu-id="57a2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a2a-119">-DefaultProfile</span></span>
<span data-ttu-id="57a2a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57a2a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a2a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a2a-121">-InputObject</span></span>
<span data-ttu-id="57a2a-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57a2a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57a2a-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="57a2a-123">-Location</span></span>
<span data-ttu-id="57a2a-124">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-124">The name of the update location.</span></span>

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

### <span data-ttu-id="57a2a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="57a2a-125">-Name</span></span>
<span data-ttu-id="57a2a-126">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="57a2a-126">Update run identifier.</span></span>

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

### <span data-ttu-id="57a2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="57a2a-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-128">Resource group name.</span></span>

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

### <span data-ttu-id="57a2a-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="57a2a-129">-SubscriptionId</span></span>
<span data-ttu-id="57a2a-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="57a2a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57a2a-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="57a2a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57a2a-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="57a2a-132">-UpdateName</span></span>
<span data-ttu-id="57a2a-133">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-133">Name of the update.</span></span>

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

### <span data-ttu-id="57a2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a2a-134">CommonParameters</span></span>
<span data-ttu-id="57a2a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57a2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a2a-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57a2a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a2a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57a2a-137">INPUTS</span></span>

### <span data-ttu-id="57a2a-138">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. ıupdateadminıdentity</span><span class="sxs-lookup"><span data-stu-id="57a2a-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="57a2a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57a2a-139">OUTPUTS</span></span>

### <span data-ttu-id="57a2a-140">Microsoft. Azure. PowerShell. cmdlet. UpdateAdmin. modeller. Api20160501. ıupdaterun</span><span class="sxs-lookup"><span data-stu-id="57a2a-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="57a2a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57a2a-141">NOTES</span></span>

<span data-ttu-id="57a2a-142">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="57a2a-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57a2a-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57a2a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="57a2a-144">INPUTOBJECT <IUpdateAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="57a2a-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57a2a-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="57a2a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57a2a-146">`[ResourceGroupName <String>]`: Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="57a2a-147">`[RunName <String>]`: Güncelleştirme çalıştırması tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="57a2a-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="57a2a-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="57a2a-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="57a2a-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57a2a-150">`[UpdateLocation <String>]`: Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="57a2a-151">`[UpdateName <String>]`: Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="57a2a-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="57a2a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57a2a-152">RELATED LINKS</span></span>

