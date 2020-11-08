---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109156"
---
# <span data-ttu-id="c0413-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c0413-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="c0413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0413-102">SYNOPSIS</span></span>
<span data-ttu-id="c0413-103">Blockzincirine üye silme.</span><span class="sxs-lookup"><span data-stu-id="c0413-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="c0413-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0413-104">SYNTAX</span></span>

### <span data-ttu-id="c0413-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0413-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0413-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c0413-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0413-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0413-107">DESCRIPTION</span></span>
<span data-ttu-id="c0413-108">Blockzincirine üye silme.</span><span class="sxs-lookup"><span data-stu-id="c0413-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="c0413-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0413-109">EXAMPLES</span></span>

### <span data-ttu-id="c0413-110">Örnek 1: blockzincir üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0413-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="c0413-111">Bu komut blockzincirine üye kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0413-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="c0413-112">Örnek 2: blockzincir üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0413-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="c0413-113">Bu komut blockzincirine üye kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0413-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="c0413-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0413-114">PARAMETERS</span></span>

### <span data-ttu-id="c0413-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c0413-115">-AsJob</span></span>
<span data-ttu-id="c0413-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c0413-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c0413-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0413-117">-DefaultProfile</span></span>
<span data-ttu-id="c0413-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0413-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0413-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0413-119">-InputObject</span></span>
<span data-ttu-id="c0413-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0413-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0413-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0413-121">-Name</span></span>
<span data-ttu-id="c0413-122">Blockzincirine üye adı</span><span class="sxs-lookup"><span data-stu-id="c0413-122">Blockchain member name</span></span>

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

### <span data-ttu-id="c0413-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0413-123">-NoWait</span></span>
<span data-ttu-id="c0413-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c0413-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c0413-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c0413-125">-PassThru</span></span>
<span data-ttu-id="c0413-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c0413-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c0413-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0413-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0413-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c0413-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c0413-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0413-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c0413-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c0413-130">-SubscriptionId</span></span>
<span data-ttu-id="c0413-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="c0413-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0413-132">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="c0413-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c0413-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0413-133">-Confirm</span></span>
<span data-ttu-id="c0413-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0413-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0413-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0413-135">-WhatIf</span></span>
<span data-ttu-id="c0413-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0413-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0413-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0413-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0413-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0413-138">CommonParameters</span></span>
<span data-ttu-id="c0413-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0413-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0413-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0413-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0413-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0413-141">INPUTS</span></span>

### <span data-ttu-id="c0413-142">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="c0413-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c0413-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0413-143">OUTPUTS</span></span>

### <span data-ttu-id="c0413-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0413-144">System.Boolean</span></span>

## <span data-ttu-id="c0413-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0413-145">NOTES</span></span>

<span data-ttu-id="c0413-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c0413-146">ALIASES</span></span>

<span data-ttu-id="c0413-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c0413-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0413-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c0413-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0413-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0413-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0413-150">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c0413-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0413-151">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="c0413-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c0413-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c0413-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0413-153">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="c0413-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c0413-154">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="c0413-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c0413-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c0413-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c0413-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0413-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c0413-157">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="c0413-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c0413-158">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="c0413-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c0413-159">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="c0413-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c0413-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0413-160">RELATED LINKS</span></span>

