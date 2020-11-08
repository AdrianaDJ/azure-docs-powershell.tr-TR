---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278738"
---
# <span data-ttu-id="be0b8-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="be0b8-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="be0b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="be0b8-103">Azure 'da karma makine kimliğini kaldırma işlemi.</span><span class="sxs-lookup"><span data-stu-id="be0b8-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="be0b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be0b8-104">SYNTAX</span></span>

### <span data-ttu-id="be0b8-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be0b8-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be0b8-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="be0b8-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be0b8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be0b8-107">DESCRIPTION</span></span>
<span data-ttu-id="be0b8-108">Azure 'da karma makine kimliğini kaldırma işlemi.</span><span class="sxs-lookup"><span data-stu-id="be0b8-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="be0b8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be0b8-109">EXAMPLES</span></span>

### <span data-ttu-id="be0b8-110">Örnek 1: bağlı bir makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="be0b8-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="be0b8-111">Bağlı makineyi siler.</span><span class="sxs-lookup"><span data-stu-id="be0b8-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="be0b8-112">Örnek 2: bağlı makineleri ardışık düzen aracılığıyla kaldırma</span><span class="sxs-lookup"><span data-stu-id="be0b8-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="be0b8-113">Kaynak grubundaki tüm makineleri kaldırır `contoso-connected-machines` .</span><span class="sxs-lookup"><span data-stu-id="be0b8-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="be0b8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be0b8-114">PARAMETERS</span></span>

### <span data-ttu-id="be0b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0b8-115">-DefaultProfile</span></span>
<span data-ttu-id="be0b8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be0b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be0b8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be0b8-117">-InputObject</span></span>
<span data-ttu-id="be0b8-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be0b8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be0b8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="be0b8-119">-Name</span></span>
<span data-ttu-id="be0b8-120">Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="be0b8-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="be0b8-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="be0b8-121">-PassThru</span></span>
<span data-ttu-id="be0b8-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="be0b8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="be0b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="be0b8-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be0b8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="be0b8-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="be0b8-125">-SubscriptionId</span></span>
<span data-ttu-id="be0b8-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="be0b8-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be0b8-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be0b8-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be0b8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="be0b8-128">-Confirm</span></span>
<span data-ttu-id="be0b8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be0b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be0b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be0b8-130">-WhatIf</span></span>
<span data-ttu-id="be0b8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be0b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be0b8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be0b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be0b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0b8-133">CommonParameters</span></span>
<span data-ttu-id="be0b8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be0b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0b8-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be0b8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0b8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be0b8-136">INPUTS</span></span>

### <span data-ttu-id="be0b8-137">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Iconnectedmachineıdentity</span><span class="sxs-lookup"><span data-stu-id="be0b8-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="be0b8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be0b8-138">OUTPUTS</span></span>

### <span data-ttu-id="be0b8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be0b8-139">System.Boolean</span></span>

## <span data-ttu-id="be0b8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be0b8-140">NOTES</span></span>

<span data-ttu-id="be0b8-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="be0b8-141">ALIASES</span></span>

<span data-ttu-id="be0b8-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="be0b8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be0b8-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="be0b8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be0b8-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be0b8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be0b8-145">INPUTOBJECT <IConnectedMachineIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="be0b8-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be0b8-146">`[ExtensionName <String>]`: Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="be0b8-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="be0b8-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="be0b8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be0b8-148">`[Name <String>]`: Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="be0b8-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="be0b8-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be0b8-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="be0b8-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="be0b8-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="be0b8-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be0b8-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="be0b8-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be0b8-152">RELATED LINKS</span></span>

