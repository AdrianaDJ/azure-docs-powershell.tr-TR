---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109096"
---
# <span data-ttu-id="6f46c-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6f46c-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="6f46c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f46c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f46c-103">Uzantıyı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="6f46c-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="6f46c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f46c-104">SYNTAX</span></span>

### <span data-ttu-id="6f46c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f46c-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6f46c-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6f46c-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f46c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f46c-107">DESCRIPTION</span></span>
<span data-ttu-id="6f46c-108">Uzantıyı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="6f46c-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="6f46c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f46c-109">EXAMPLES</span></span>

### <span data-ttu-id="6f46c-110">Örnek 1: bir makine uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6f46c-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="6f46c-111">Makinede uzantıyı siler.</span><span class="sxs-lookup"><span data-stu-id="6f46c-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="6f46c-112">Örnek 2: ardışık düzen aracılığıyla uzantıyı kaldırın</span><span class="sxs-lookup"><span data-stu-id="6f46c-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="6f46c-113">Belirtilen makinedeki tüm uzantıları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f46c-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="6f46c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f46c-114">PARAMETERS</span></span>

### <span data-ttu-id="6f46c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6f46c-115">-AsJob</span></span>
<span data-ttu-id="6f46c-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="6f46c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6f46c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f46c-117">-DefaultProfile</span></span>
<span data-ttu-id="6f46c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f46c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f46c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f46c-119">-InputObject</span></span>
<span data-ttu-id="6f46c-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6f46c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f46c-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="6f46c-121">-MachineName</span></span>
<span data-ttu-id="6f46c-122">Uzantının silinmesi gereken makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="6f46c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f46c-123">-Name</span></span>
<span data-ttu-id="6f46c-124">Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="6f46c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6f46c-125">-NoWait</span></span>
<span data-ttu-id="6f46c-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="6f46c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6f46c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6f46c-127">-PassThru</span></span>
<span data-ttu-id="6f46c-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="6f46c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6f46c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f46c-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f46c-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f46c-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6f46c-131">-SubscriptionId</span></span>
<span data-ttu-id="6f46c-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6f46c-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6f46c-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f46c-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6f46c-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f46c-134">-Confirm</span></span>
<span data-ttu-id="6f46c-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f46c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f46c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f46c-136">-WhatIf</span></span>
<span data-ttu-id="6f46c-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f46c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f46c-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f46c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f46c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f46c-139">CommonParameters</span></span>
<span data-ttu-id="6f46c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f46c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f46c-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f46c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f46c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f46c-142">INPUTS</span></span>

### <span data-ttu-id="6f46c-143">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Iconnectedmachineıdentity</span><span class="sxs-lookup"><span data-stu-id="6f46c-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="6f46c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f46c-144">OUTPUTS</span></span>

### <span data-ttu-id="6f46c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f46c-145">System.Boolean</span></span>

## <span data-ttu-id="6f46c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f46c-146">NOTES</span></span>

<span data-ttu-id="6f46c-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6f46c-147">ALIASES</span></span>

<span data-ttu-id="6f46c-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6f46c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f46c-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6f46c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f46c-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6f46c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f46c-151">INPUTOBJECT <IConnectedMachineIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6f46c-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f46c-152">`[ExtensionName <String>]`: Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="6f46c-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6f46c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f46c-154">`[Name <String>]`: Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="6f46c-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6f46c-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6f46c-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6f46c-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6f46c-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f46c-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6f46c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f46c-158">RELATED LINKS</span></span>

