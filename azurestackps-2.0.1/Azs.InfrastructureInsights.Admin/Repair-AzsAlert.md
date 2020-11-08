---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105221"
---
# <span data-ttu-id="c38c9-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c38c9-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="c38c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c38c9-103">Bir uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="c38c9-103">Repairs an alert.</span></span>

## <span data-ttu-id="c38c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c38c9-104">SYNTAX</span></span>

### <span data-ttu-id="c38c9-105">Onar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c38c9-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c38c9-106">Repairviadentity</span><span class="sxs-lookup"><span data-stu-id="c38c9-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c38c9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c38c9-107">DESCRIPTION</span></span>
<span data-ttu-id="c38c9-108">Bir uyarıyı onarır.</span><span class="sxs-lookup"><span data-stu-id="c38c9-108">Repairs an alert.</span></span>

## <span data-ttu-id="c38c9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c38c9-109">EXAMPLES</span></span>

### <span data-ttu-id="c38c9-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="c38c9-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="c38c9-111">Uyarıyı adıyla onarır.</span><span class="sxs-lookup"><span data-stu-id="c38c9-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="c38c9-112">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="c38c9-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="c38c9-113">Bir uyarıyı boru üzerinden onarır.</span><span class="sxs-lookup"><span data-stu-id="c38c9-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="c38c9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c38c9-114">PARAMETERS</span></span>

### <span data-ttu-id="c38c9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c38c9-115">-AsJob</span></span>
<span data-ttu-id="c38c9-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c38c9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c38c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38c9-117">-DefaultProfile</span></span>
<span data-ttu-id="c38c9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c38c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c38c9-119">-InputObject</span></span>
<span data-ttu-id="c38c9-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c38c9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c38c9-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="c38c9-121">-Location</span></span>
<span data-ttu-id="c38c9-122">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="c38c9-122">Name of the region</span></span>

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

### <span data-ttu-id="c38c9-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c38c9-123">-Name</span></span>
<span data-ttu-id="c38c9-124">Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="c38c9-124">Name of the alert.</span></span>

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

### <span data-ttu-id="c38c9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c38c9-125">-NoWait</span></span>
<span data-ttu-id="c38c9-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c38c9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c38c9-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c38c9-127">-PassThru</span></span>
<span data-ttu-id="c38c9-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c38c9-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c38c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="c38c9-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c38c9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c38c9-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c38c9-131">-SubscriptionId</span></span>
<span data-ttu-id="c38c9-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c38c9-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c38c9-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c38c9-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c38c9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c38c9-134">-Confirm</span></span>
<span data-ttu-id="c38c9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c38c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38c9-136">-WhatIf</span></span>
<span data-ttu-id="c38c9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c38c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38c9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c38c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38c9-139">CommonParameters</span></span>
<span data-ttu-id="c38c9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c38c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38c9-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c38c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38c9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c38c9-142">INPUTS</span></span>

### <span data-ttu-id="c38c9-143">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c38c9-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="c38c9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c38c9-144">OUTPUTS</span></span>

### <span data-ttu-id="c38c9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c38c9-145">System.Boolean</span></span>



## <span data-ttu-id="c38c9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c38c9-146">NOTES</span></span>

<span data-ttu-id="c38c9-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c38c9-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c38c9-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c38c9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c38c9-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c38c9-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c38c9-150">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="c38c9-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="c38c9-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c38c9-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c38c9-152">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="c38c9-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="c38c9-153">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c38c9-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c38c9-154">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c38c9-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="c38c9-155">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="c38c9-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="c38c9-156">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c38c9-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="c38c9-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c38c9-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c38c9-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c38c9-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c38c9-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c38c9-159">RELATED LINKS</span></span>

