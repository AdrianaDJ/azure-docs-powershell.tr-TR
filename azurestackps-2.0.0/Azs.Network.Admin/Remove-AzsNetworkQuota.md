---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935983"
---
# <span data-ttu-id="2ea57-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="2ea57-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="2ea57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea57-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea57-103">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="2ea57-103">Delete a quota by name.</span></span>

## <span data-ttu-id="2ea57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ea57-104">SYNTAX</span></span>

### <span data-ttu-id="2ea57-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ea57-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ea57-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="2ea57-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ea57-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ea57-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea57-108">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="2ea57-108">Delete a quota by name.</span></span>

## <span data-ttu-id="2ea57-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ea57-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea57-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2ea57-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="2ea57-111">Ağ kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="2ea57-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="2ea57-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2ea57-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="2ea57-113">Kanal kullanarak ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="2ea57-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="2ea57-114">--------------------------ÖRNEK 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="2ea57-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="2ea57-115">Ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="2ea57-115">Remove a network quota.</span></span>

## <span data-ttu-id="2ea57-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ea57-116">PARAMETERS</span></span>

### <span data-ttu-id="2ea57-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ea57-117">-AsJob</span></span>
<span data-ttu-id="2ea57-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="2ea57-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2ea57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea57-119">-DefaultProfile</span></span>
<span data-ttu-id="2ea57-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ea57-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea57-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea57-121">-InputObject</span></span>
<span data-ttu-id="2ea57-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ea57-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2ea57-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="2ea57-123">-Location</span></span>
<span data-ttu-id="2ea57-124">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2ea57-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea57-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ea57-125">-Name</span></span>
<span data-ttu-id="2ea57-126">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="2ea57-126">Name of the resource.</span></span>

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

### <span data-ttu-id="2ea57-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ea57-127">-NoWait</span></span>
<span data-ttu-id="2ea57-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="2ea57-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ea57-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ea57-129">-PassThru</span></span>
<span data-ttu-id="2ea57-130">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="2ea57-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2ea57-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2ea57-131">-SubscriptionId</span></span>
<span data-ttu-id="2ea57-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2ea57-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ea57-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ea57-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2ea57-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ea57-134">-Confirm</span></span>
<span data-ttu-id="2ea57-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ea57-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea57-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea57-136">-WhatIf</span></span>
<span data-ttu-id="2ea57-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ea57-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea57-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ea57-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea57-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea57-139">CommonParameters</span></span>
<span data-ttu-id="2ea57-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ea57-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea57-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ea57-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea57-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ea57-142">INPUTS</span></span>

### <span data-ttu-id="2ea57-143">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. ınetworkadminıdentity</span><span class="sxs-lookup"><span data-stu-id="2ea57-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="2ea57-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ea57-144">OUTPUTS</span></span>

### <span data-ttu-id="2ea57-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ea57-145">System.Boolean</span></span>



## <span data-ttu-id="2ea57-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ea57-146">NOTES</span></span>

<span data-ttu-id="2ea57-147">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ea57-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ea57-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ea57-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2ea57-149">INPUTOBJECT <INetworkAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="2ea57-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ea57-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="2ea57-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ea57-151">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2ea57-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2ea57-152">`[ResourceName <String>]`: Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="2ea57-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="2ea57-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="2ea57-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2ea57-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ea57-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2ea57-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ea57-155">RELATED LINKS</span></span>

