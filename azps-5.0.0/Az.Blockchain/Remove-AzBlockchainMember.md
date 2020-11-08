---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276811"
---
# <span data-ttu-id="34d14-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="34d14-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="34d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d14-102">SYNOPSIS</span></span>
<span data-ttu-id="34d14-103">Blockzincirine üye silme.</span><span class="sxs-lookup"><span data-stu-id="34d14-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="34d14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34d14-104">SYNTAX</span></span>

### <span data-ttu-id="34d14-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34d14-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34d14-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="34d14-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34d14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34d14-107">DESCRIPTION</span></span>
<span data-ttu-id="34d14-108">Blockzincirine üye silme.</span><span class="sxs-lookup"><span data-stu-id="34d14-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="34d14-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34d14-109">EXAMPLES</span></span>

### <span data-ttu-id="34d14-110">Örnek 1: blockzincir üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="34d14-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="34d14-111">Bu komut blockzincirine üye kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34d14-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="34d14-112">Örnek 2: blockzincir üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="34d14-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="34d14-113">Bu komut blockzincirine üye kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34d14-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="34d14-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34d14-114">PARAMETERS</span></span>

### <span data-ttu-id="34d14-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="34d14-115">-AsJob</span></span>
<span data-ttu-id="34d14-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="34d14-116">Run the command as a job</span></span>

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

### <span data-ttu-id="34d14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d14-117">-DefaultProfile</span></span>
<span data-ttu-id="34d14-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34d14-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d14-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34d14-119">-InputObject</span></span>
<span data-ttu-id="34d14-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34d14-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34d14-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="34d14-121">-Name</span></span>
<span data-ttu-id="34d14-122">Blockzincirine üye adı</span><span class="sxs-lookup"><span data-stu-id="34d14-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d14-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="34d14-123">-NoWait</span></span>
<span data-ttu-id="34d14-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="34d14-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34d14-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34d14-125">-PassThru</span></span>
<span data-ttu-id="34d14-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="34d14-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34d14-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d14-127">-ResourceGroupName</span></span>
<span data-ttu-id="34d14-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34d14-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="34d14-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34d14-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="34d14-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="34d14-130">-SubscriptionId</span></span>
<span data-ttu-id="34d14-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="34d14-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="34d14-132">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="34d14-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="34d14-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="34d14-133">-Confirm</span></span>
<span data-ttu-id="34d14-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34d14-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d14-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d14-135">-WhatIf</span></span>
<span data-ttu-id="34d14-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34d14-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d14-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34d14-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d14-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d14-138">CommonParameters</span></span>
<span data-ttu-id="34d14-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34d14-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d14-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34d14-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d14-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34d14-141">INPUTS</span></span>

### <span data-ttu-id="34d14-142">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="34d14-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="34d14-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34d14-143">OUTPUTS</span></span>

### <span data-ttu-id="34d14-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34d14-144">System.Boolean</span></span>

## <span data-ttu-id="34d14-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34d14-145">NOTES</span></span>

<span data-ttu-id="34d14-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="34d14-146">ALIASES</span></span>

<span data-ttu-id="34d14-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="34d14-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34d14-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34d14-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34d14-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34d14-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34d14-150">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="34d14-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34d14-151">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="34d14-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="34d14-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="34d14-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34d14-153">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="34d14-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="34d14-154">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="34d14-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="34d14-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34d14-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="34d14-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34d14-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="34d14-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="34d14-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="34d14-158">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="34d14-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="34d14-159">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="34d14-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="34d14-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34d14-160">RELATED LINKS</span></span>

