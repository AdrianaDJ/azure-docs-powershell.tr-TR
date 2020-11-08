---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107809"
---
# <span data-ttu-id="34982-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="34982-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="34982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34982-102">SYNOPSIS</span></span>
<span data-ttu-id="34982-103">Çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="34982-103">Deletes the workspace.</span></span>

## <span data-ttu-id="34982-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34982-104">SYNTAX</span></span>

### <span data-ttu-id="34982-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34982-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34982-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="34982-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34982-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34982-107">DESCRIPTION</span></span>
<span data-ttu-id="34982-108">Çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="34982-108">Deletes the workspace.</span></span>

## <span data-ttu-id="34982-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34982-109">EXAMPLES</span></span>

### <span data-ttu-id="34982-110">Örnek 1: Veriricks çalışma alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="34982-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="34982-111">Bu komut, kaynak grubundan Veriricks çalışma alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34982-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="34982-112">Örnek 2: nesneleri nesne bazında Veriricleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="34982-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="34982-113">Bu komut, kaynak grubundan Veriricks çalışma alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34982-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="34982-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34982-114">PARAMETERS</span></span>

### <span data-ttu-id="34982-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="34982-115">-AsJob</span></span>
<span data-ttu-id="34982-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="34982-116">Run the command as a job</span></span>

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

### <span data-ttu-id="34982-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34982-117">-DefaultProfile</span></span>
<span data-ttu-id="34982-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34982-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34982-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34982-119">-InputObject</span></span>
<span data-ttu-id="34982-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34982-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34982-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="34982-121">-Name</span></span>
<span data-ttu-id="34982-122">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="34982-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34982-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="34982-123">-NoWait</span></span>
<span data-ttu-id="34982-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="34982-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34982-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34982-125">-PassThru</span></span>
<span data-ttu-id="34982-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="34982-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34982-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34982-127">-ResourceGroupName</span></span>
<span data-ttu-id="34982-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34982-128">The name of the resource group.</span></span>
<span data-ttu-id="34982-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="34982-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34982-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="34982-130">-SubscriptionId</span></span>
<span data-ttu-id="34982-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34982-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34982-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="34982-132">-Confirm</span></span>
<span data-ttu-id="34982-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34982-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34982-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34982-134">-WhatIf</span></span>
<span data-ttu-id="34982-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34982-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34982-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34982-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34982-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34982-137">CommonParameters</span></span>
<span data-ttu-id="34982-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34982-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34982-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34982-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34982-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34982-140">INPUTS</span></span>

### <span data-ttu-id="34982-141">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="34982-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="34982-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34982-142">OUTPUTS</span></span>

### <span data-ttu-id="34982-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34982-143">System.Boolean</span></span>

## <span data-ttu-id="34982-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34982-144">NOTES</span></span>

<span data-ttu-id="34982-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="34982-145">ALIASES</span></span>

<span data-ttu-id="34982-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="34982-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34982-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34982-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34982-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34982-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34982-149">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="34982-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34982-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="34982-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34982-151">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="34982-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="34982-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34982-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34982-153">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="34982-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="34982-154">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34982-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34982-155">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="34982-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="34982-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34982-156">RELATED LINKS</span></span>

