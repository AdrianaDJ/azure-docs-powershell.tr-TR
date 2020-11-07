---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936003"
---
# <span data-ttu-id="b501c-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="b501c-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="b501c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b501c-102">SYNOPSIS</span></span>
<span data-ttu-id="b501c-103">Bir uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="b501c-103">Repairs an alert.</span></span>

## <span data-ttu-id="b501c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b501c-104">SYNTAX</span></span>

### <span data-ttu-id="b501c-105">Onar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b501c-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b501c-106">Repairviadentity</span><span class="sxs-lookup"><span data-stu-id="b501c-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b501c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b501c-107">DESCRIPTION</span></span>
<span data-ttu-id="b501c-108">Bir uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="b501c-108">Repairs an alert.</span></span>

## <span data-ttu-id="b501c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b501c-109">EXAMPLES</span></span>

### <span data-ttu-id="b501c-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="b501c-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="b501c-111">Uyarıyı adıyla onarır.</span><span class="sxs-lookup"><span data-stu-id="b501c-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="b501c-112">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="b501c-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="b501c-113">Bir uyarıyı boru üzerinden onarır.</span><span class="sxs-lookup"><span data-stu-id="b501c-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="b501c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b501c-114">PARAMETERS</span></span>

### <span data-ttu-id="b501c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b501c-115">-AsJob</span></span>
<span data-ttu-id="b501c-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="b501c-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b501c-117">-DefaultProfile</span></span>
<span data-ttu-id="b501c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b501c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b501c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b501c-119">-InputObject</span></span>
<span data-ttu-id="b501c-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b501c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="b501c-121">-Location</span></span>
<span data-ttu-id="b501c-122">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="b501c-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b501c-123">-Name</span></span>
<span data-ttu-id="b501c-124">Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="b501c-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b501c-125">-NoWait</span></span>
<span data-ttu-id="b501c-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="b501c-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b501c-127">-PassThru</span></span>
<span data-ttu-id="b501c-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="b501c-128">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b501c-129">-ResourceGroupName</span></span>
<span data-ttu-id="b501c-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b501c-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b501c-131">-SubscriptionId</span></span>
<span data-ttu-id="b501c-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="b501c-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b501c-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b501c-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b501c-134">-Confirm</span></span>
<span data-ttu-id="b501c-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b501c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b501c-136">-WhatIf</span></span>
<span data-ttu-id="b501c-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b501c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b501c-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b501c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b501c-139">CommonParameters</span></span>
<span data-ttu-id="b501c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b501c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b501c-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b501c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b501c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b501c-142">INPUTS</span></span>

### <span data-ttu-id="b501c-143">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b501c-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="b501c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b501c-144">OUTPUTS</span></span>

### <span data-ttu-id="b501c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b501c-145">System.Boolean</span></span>



## <span data-ttu-id="b501c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b501c-146">NOTES</span></span>

<span data-ttu-id="b501c-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b501c-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b501c-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b501c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b501c-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b501c-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b501c-150">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="b501c-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="b501c-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b501c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b501c-152">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="b501c-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="b501c-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b501c-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b501c-154">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b501c-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="b501c-155">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="b501c-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="b501c-156">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b501c-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="b501c-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="b501c-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b501c-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b501c-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b501c-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b501c-159">RELATED LINKS</span></span>

