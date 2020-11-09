---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320177"
---
# <span data-ttu-id="c3f72-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="c3f72-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="c3f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3f72-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f72-103">Belirtilen abonelikteki adanmış bir HSM 'yi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c3f72-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="c3f72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3f72-104">SYNTAX</span></span>

### <span data-ttu-id="c3f72-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3f72-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3f72-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="c3f72-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3f72-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3f72-107">DESCRIPTION</span></span>
<span data-ttu-id="c3f72-108">Belirtilen abonelikteki adanmış bir HSM 'yi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c3f72-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="c3f72-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3f72-109">EXAMPLES</span></span>

### <span data-ttu-id="c3f72-110">Örnek 1: adanmış HSM 'nin parametre etiketini adla güncelleyin</span><span class="sxs-lookup"><span data-stu-id="c3f72-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="c3f72-111">Bu komut, adanmış HSM 'nin parametre etiketini ada göre güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c3f72-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="c3f72-112">Örnek 2: adanmış HSM nesnesinin parametre etiketini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c3f72-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="c3f72-113">Bu komut, adanmış HSM 'nin nesne etiketini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c3f72-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="c3f72-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3f72-114">PARAMETERS</span></span>

### <span data-ttu-id="c3f72-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c3f72-115">-AsJob</span></span>
<span data-ttu-id="c3f72-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c3f72-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c3f72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f72-117">-DefaultProfile</span></span>
<span data-ttu-id="c3f72-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3f72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3f72-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3f72-119">-InputObject</span></span>
<span data-ttu-id="c3f72-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3f72-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f72-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3f72-121">-Name</span></span>
<span data-ttu-id="c3f72-122">Adanmış HSM adı</span><span class="sxs-lookup"><span data-stu-id="c3f72-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f72-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3f72-123">-NoWait</span></span>
<span data-ttu-id="c3f72-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c3f72-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3f72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f72-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3f72-126">Sunucunun ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3f72-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f72-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c3f72-127">-SubscriptionId</span></span>
<span data-ttu-id="c3f72-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c3f72-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3f72-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3f72-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f72-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c3f72-130">-Tag</span></span>
<span data-ttu-id="c3f72-131">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="c3f72-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f72-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3f72-132">-Confirm</span></span>
<span data-ttu-id="c3f72-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3f72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f72-134">-WhatIf</span></span>
<span data-ttu-id="c3f72-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3f72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f72-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3f72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f72-137">CommonParameters</span></span>
<span data-ttu-id="c3f72-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3f72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f72-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3f72-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f72-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3f72-140">INPUTS</span></span>

### <span data-ttu-id="c3f72-141">Microsoft. Azure. PowerShell. cmdlet. (".</span><span class="sxs-lookup"><span data-stu-id="c3f72-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="c3f72-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3f72-142">OUTPUTS</span></span>

### <span data-ttu-id="c3f72-143">Microsoft. Azure. PowerShell. cmdlet. ayrılmış Atedhsm. modeller. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="c3f72-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="c3f72-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3f72-144">NOTES</span></span>

<span data-ttu-id="c3f72-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c3f72-145">ALIASES</span></span>

<span data-ttu-id="c3f72-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c3f72-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3f72-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3f72-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3f72-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3f72-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3f72-149">INPUTOBJECT <IDedicatedHsmIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c3f72-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3f72-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c3f72-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3f72-151">`[Name <String>]`: Adanmış HSM 'nin adı</span><span class="sxs-lookup"><span data-stu-id="c3f72-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="c3f72-152">`[ResourceGroupName <String>]`: Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3f72-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="c3f72-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c3f72-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c3f72-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3f72-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c3f72-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3f72-155">RELATED LINKS</span></span>

