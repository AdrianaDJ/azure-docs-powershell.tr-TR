---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279101"
---
# <span data-ttu-id="ba814-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="ba814-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="ba814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba814-102">SYNOPSIS</span></span>
<span data-ttu-id="ba814-103">İşlem düğümünü silin.</span><span class="sxs-lookup"><span data-stu-id="ba814-103">Delete the transaction node.</span></span>

## <span data-ttu-id="ba814-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba814-104">SYNTAX</span></span>

### <span data-ttu-id="ba814-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba814-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ba814-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ba814-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba814-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba814-107">DESCRIPTION</span></span>
<span data-ttu-id="ba814-108">İşlem düğümünü silin.</span><span class="sxs-lookup"><span data-stu-id="ba814-108">Delete the transaction node.</span></span>

## <span data-ttu-id="ba814-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba814-109">EXAMPLES</span></span>

### <span data-ttu-id="ba814-110">Örnek 1: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="ba814-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="ba814-111">Bu komut, işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba814-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="ba814-112">Örnek 2: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="ba814-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="ba814-113">Bu komut, işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba814-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="ba814-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba814-114">PARAMETERS</span></span>

### <span data-ttu-id="ba814-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ba814-115">-AsJob</span></span>
<span data-ttu-id="ba814-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="ba814-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ba814-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="ba814-117">-BlockchainMemberName</span></span>
<span data-ttu-id="ba814-118">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="ba814-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba814-119">-DefaultProfile</span></span>
<span data-ttu-id="ba814-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba814-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba814-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba814-121">-InputObject</span></span>
<span data-ttu-id="ba814-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba814-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba814-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba814-123">-Name</span></span>
<span data-ttu-id="ba814-124">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba814-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba814-125">-NoWait</span></span>
<span data-ttu-id="ba814-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="ba814-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba814-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba814-127">-PassThru</span></span>
<span data-ttu-id="ba814-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="ba814-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba814-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba814-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba814-130">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ba814-131">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba814-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ba814-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ba814-132">-SubscriptionId</span></span>
<span data-ttu-id="ba814-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="ba814-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba814-134">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ba814-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba814-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba814-135">-Confirm</span></span>
<span data-ttu-id="ba814-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba814-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba814-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba814-137">-WhatIf</span></span>
<span data-ttu-id="ba814-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba814-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba814-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba814-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba814-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba814-140">CommonParameters</span></span>
<span data-ttu-id="ba814-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba814-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba814-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba814-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba814-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba814-143">INPUTS</span></span>

### <span data-ttu-id="ba814-144">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity</span><span class="sxs-lookup"><span data-stu-id="ba814-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ba814-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba814-145">OUTPUTS</span></span>

### <span data-ttu-id="ba814-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba814-146">System.Boolean</span></span>

## <span data-ttu-id="ba814-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba814-147">NOTES</span></span>

<span data-ttu-id="ba814-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ba814-148">ALIASES</span></span>

<span data-ttu-id="ba814-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ba814-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba814-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba814-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba814-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba814-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba814-152">INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ba814-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba814-153">`[BlockchainMemberName <String>]`: Blockzincirine üye adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ba814-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ba814-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba814-155">`[Location <String>]`: Konum adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ba814-156">`[OperationId <String>]`: İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="ba814-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ba814-157">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ba814-158">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba814-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ba814-159">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="ba814-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ba814-160">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ba814-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ba814-161">`[TransactionNodeName <String>]`: İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="ba814-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ba814-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba814-162">RELATED LINKS</span></span>

