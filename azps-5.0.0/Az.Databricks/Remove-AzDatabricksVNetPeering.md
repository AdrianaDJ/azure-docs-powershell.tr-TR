---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320206"
---
# <span data-ttu-id="c97b9-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="c97b9-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="c97b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c97b9-103">Çalışma alanı Vneteşleme 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="c97b9-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="c97b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c97b9-104">SYNTAX</span></span>

### <span data-ttu-id="c97b9-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c97b9-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c97b9-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c97b9-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c97b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c97b9-107">DESCRIPTION</span></span>
<span data-ttu-id="c97b9-108">Çalışma alanı Vneteşleme 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="c97b9-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="c97b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c97b9-109">EXAMPLES</span></span>

### <span data-ttu-id="c97b9-110">Örnek 1: ad ile verieşlerinin VNET eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c97b9-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="c97b9-111">Bu komut, verieşlerinin VNET eşleme adını adıyla kaldırır</span><span class="sxs-lookup"><span data-stu-id="c97b9-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="c97b9-112">Örnek 2: nesneye göre verieşlerinin VNET eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c97b9-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="c97b9-113">Bu komut, nesne tarafından verieşlerinin VNET eşliğini kaldırır</span><span class="sxs-lookup"><span data-stu-id="c97b9-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="c97b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c97b9-114">PARAMETERS</span></span>

### <span data-ttu-id="c97b9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c97b9-115">-AsJob</span></span>
<span data-ttu-id="c97b9-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c97b9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c97b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97b9-117">-DefaultProfile</span></span>
<span data-ttu-id="c97b9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c97b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97b9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c97b9-119">-InputObject</span></span>
<span data-ttu-id="c97b9-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c97b9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c97b9-121">-Name</span></span>
<span data-ttu-id="c97b9-122">Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="c97b9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c97b9-123">-NoWait</span></span>
<span data-ttu-id="c97b9-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c97b9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c97b9-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c97b9-125">-PassThru</span></span>
<span data-ttu-id="c97b9-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c97b9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c97b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="c97b9-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-128">The name of the resource group.</span></span>
<span data-ttu-id="c97b9-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c97b9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c97b9-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c97b9-130">-SubscriptionId</span></span>
<span data-ttu-id="c97b9-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c97b9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c97b9-132">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c97b9-132">-WorkspaceName</span></span>
<span data-ttu-id="c97b9-133">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="c97b9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c97b9-134">-Confirm</span></span>
<span data-ttu-id="c97b9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c97b9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97b9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97b9-136">-WhatIf</span></span>
<span data-ttu-id="c97b9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c97b9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97b9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c97b9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97b9-139">CommonParameters</span></span>
<span data-ttu-id="c97b9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c97b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97b9-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c97b9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97b9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c97b9-142">INPUTS</span></span>

### <span data-ttu-id="c97b9-143">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="c97b9-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c97b9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c97b9-144">OUTPUTS</span></span>

### <span data-ttu-id="c97b9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c97b9-145">System.Boolean</span></span>

## <span data-ttu-id="c97b9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c97b9-146">NOTES</span></span>

<span data-ttu-id="c97b9-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c97b9-147">ALIASES</span></span>

<span data-ttu-id="c97b9-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c97b9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c97b9-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c97b9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c97b9-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c97b9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c97b9-151">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c97b9-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c97b9-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c97b9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c97b9-153">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c97b9-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c97b9-155">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c97b9-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="c97b9-156">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c97b9-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c97b9-157">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="c97b9-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c97b9-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c97b9-158">RELATED LINKS</span></span>

