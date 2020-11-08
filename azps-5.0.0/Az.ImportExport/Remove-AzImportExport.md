---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277366"
---
# <span data-ttu-id="a9e99-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a9e99-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="a9e99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e99-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e99-103">Var olan bir işi siler.</span><span class="sxs-lookup"><span data-stu-id="a9e99-103">Deletes an existing job.</span></span>
<span data-ttu-id="a9e99-104">Yalnızca oluşturma veya tamamlanan durumlarındaki işler silinebilir.</span><span class="sxs-lookup"><span data-stu-id="a9e99-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="a9e99-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9e99-105">SYNTAX</span></span>

### <span data-ttu-id="a9e99-106">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9e99-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9e99-107">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a9e99-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9e99-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9e99-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e99-109">Var olan bir işi siler.</span><span class="sxs-lookup"><span data-stu-id="a9e99-109">Deletes an existing job.</span></span>
<span data-ttu-id="a9e99-110">Yalnızca oluşturma veya tamamlanan durumlarındaki işler silinebilir.</span><span class="sxs-lookup"><span data-stu-id="a9e99-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="a9e99-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9e99-111">EXAMPLES</span></span>

### <span data-ttu-id="a9e99-112">Örnek 1: resourceGroup ve sunucu adına göre ımportexport işini kaldırın</span><span class="sxs-lookup"><span data-stu-id="a9e99-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="a9e99-113">Bu cmdlet, resourceGroup ve sunucu adına göre ımportexport işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9e99-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="a9e99-114">Örnek 2: kimliğe göre ımportexport işini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a9e99-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="a9e99-115">Bu cmdlet ımportexport işini Identity 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9e99-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="a9e99-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9e99-116">PARAMETERS</span></span>

### <span data-ttu-id="a9e99-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a9e99-117">-AcceptLanguage</span></span>
<span data-ttu-id="a9e99-118">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e99-118">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e99-119">-DefaultProfile</span></span>
<span data-ttu-id="a9e99-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9e99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e99-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9e99-121">-InputObject</span></span>
<span data-ttu-id="a9e99-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9e99-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e99-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9e99-123">-Name</span></span>
<span data-ttu-id="a9e99-124">İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="a9e99-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e99-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a9e99-125">-PassThru</span></span>
<span data-ttu-id="a9e99-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="a9e99-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a9e99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e99-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9e99-128">Kaynak grubu adı, kullanıcı aboneliği içinde kaynak grubunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a9e99-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="a9e99-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a9e99-129">-SubscriptionId</span></span>
<span data-ttu-id="a9e99-130">Azure kullanıcısına ait abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a9e99-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="a9e99-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9e99-131">-Confirm</span></span>
<span data-ttu-id="a9e99-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9e99-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e99-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e99-133">-WhatIf</span></span>
<span data-ttu-id="a9e99-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9e99-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e99-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9e99-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e99-136">CommonParameters</span></span>
<span data-ttu-id="a9e99-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9e99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e99-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a9e99-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e99-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9e99-139">INPUTS</span></span>

### <span data-ttu-id="a9e99-140">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. ıımportexportidentity</span><span class="sxs-lookup"><span data-stu-id="a9e99-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="a9e99-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9e99-141">OUTPUTS</span></span>

### <span data-ttu-id="a9e99-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9e99-142">System.Boolean</span></span>

## <span data-ttu-id="a9e99-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9e99-143">NOTES</span></span>

<span data-ttu-id="a9e99-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a9e99-144">ALIASES</span></span>

<span data-ttu-id="a9e99-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a9e99-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9e99-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a9e99-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9e99-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9e99-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9e99-148">INPUTOBJECT <IImportExportIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a9e99-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9e99-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a9e99-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9e99-150">`[JobName <String>]`: İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="a9e99-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="a9e99-151">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="a9e99-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="a9e99-152">Örneğin, Batı ABD veya westus.</span><span class="sxs-lookup"><span data-stu-id="a9e99-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="a9e99-153">`[ResourceGroupName <String>]`: Kaynak grubu adı, kaynak grubunu Kullanıcı aboneliğindeki benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a9e99-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="a9e99-154">`[SubscriptionId <String>]`: Azure kullanıcısının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a9e99-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="a9e99-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9e99-155">RELATED LINKS</span></span>

