---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320189"
---
# <span data-ttu-id="c1491-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="c1491-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="c1491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1491-102">SYNOPSIS</span></span>
<span data-ttu-id="c1491-103">Belirtilen Azure adanmış HSM 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="c1491-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="c1491-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1491-104">SYNTAX</span></span>

### <span data-ttu-id="c1491-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1491-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1491-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c1491-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1491-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1491-107">DESCRIPTION</span></span>
<span data-ttu-id="c1491-108">Belirtilen Azure adanmış HSM 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="c1491-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="c1491-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1491-109">EXAMPLES</span></span>

### <span data-ttu-id="c1491-110">Örnek 1: adanmış bir HSM 'yi adla kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1491-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="c1491-111">Bu işlem, bir donanım güvenlik modülünü (HSM) ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1491-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="c1491-112">Örnek 2: adanmış bir HSM 'yi nesneye kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1491-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="c1491-113">Bu işlem, adanmış bir HSM nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1491-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="c1491-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1491-114">PARAMETERS</span></span>

### <span data-ttu-id="c1491-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c1491-115">-AsJob</span></span>
<span data-ttu-id="c1491-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c1491-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c1491-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1491-117">-DefaultProfile</span></span>
<span data-ttu-id="c1491-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1491-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1491-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1491-119">-InputObject</span></span>
<span data-ttu-id="c1491-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1491-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1491-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1491-121">-Name</span></span>
<span data-ttu-id="c1491-122">Silinecek adanmış HSM 'nin adı</span><span class="sxs-lookup"><span data-stu-id="c1491-122">The name of the dedicated HSM to delete</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1491-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c1491-123">-NoWait</span></span>
<span data-ttu-id="c1491-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c1491-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1491-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c1491-125">-PassThru</span></span>
<span data-ttu-id="c1491-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c1491-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c1491-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1491-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1491-128">Adanmış HSM 'nin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c1491-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1491-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c1491-129">-SubscriptionId</span></span>
<span data-ttu-id="c1491-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c1491-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c1491-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c1491-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1491-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1491-132">-Confirm</span></span>
<span data-ttu-id="c1491-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1491-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1491-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1491-134">-WhatIf</span></span>
<span data-ttu-id="c1491-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1491-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1491-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1491-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1491-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1491-137">CommonParameters</span></span>
<span data-ttu-id="c1491-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1491-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1491-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1491-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1491-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1491-140">INPUTS</span></span>

### <span data-ttu-id="c1491-141">Microsoft. Azure. PowerShell. cmdlet. (".</span><span class="sxs-lookup"><span data-stu-id="c1491-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="c1491-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1491-142">OUTPUTS</span></span>

### <span data-ttu-id="c1491-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1491-143">System.Boolean</span></span>

## <span data-ttu-id="c1491-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1491-144">NOTES</span></span>

<span data-ttu-id="c1491-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c1491-145">ALIASES</span></span>

<span data-ttu-id="c1491-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c1491-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1491-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c1491-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1491-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1491-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1491-149">INPUTOBJECT <IDedicatedHsmIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c1491-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c1491-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c1491-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1491-151">`[Name <String>]`: Adanmış HSM 'nin adı</span><span class="sxs-lookup"><span data-stu-id="c1491-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="c1491-152">`[ResourceGroupName <String>]`: Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c1491-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="c1491-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c1491-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c1491-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c1491-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c1491-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1491-155">RELATED LINKS</span></span>

