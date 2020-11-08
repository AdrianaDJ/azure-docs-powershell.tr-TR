---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268225"
---
# <span data-ttu-id="ddce5-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="ddce5-101">Get-AzImportExport</span></span>

## <span data-ttu-id="ddce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddce5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddce5-103">Var olan bir iş hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ddce5-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="ddce5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddce5-104">SYNTAX</span></span>

### <span data-ttu-id="ddce5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddce5-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ddce5-106">Al</span><span class="sxs-lookup"><span data-stu-id="ddce5-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ddce5-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ddce5-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ddce5-108">List1</span><span class="sxs-lookup"><span data-stu-id="ddce5-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ddce5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddce5-109">DESCRIPTION</span></span>
<span data-ttu-id="ddce5-110">Var olan bir iş hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ddce5-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="ddce5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddce5-111">EXAMPLES</span></span>

### <span data-ttu-id="ddce5-112">Örnek 1: varsayılan içerikle ımportexport işini alma</span><span class="sxs-lookup"><span data-stu-id="ddce5-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ddce5-113">Bu cmdlet, ımportexport işini varsayılan içerikle alır.</span><span class="sxs-lookup"><span data-stu-id="ddce5-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="ddce5-114">Örnek 2: kaynak grubuna ve iş adına göre ımportexport işini alma</span><span class="sxs-lookup"><span data-stu-id="ddce5-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ddce5-115">Bu cmdlet, kaynak grubuna ve iş adına göre ımportexport işini alır.</span><span class="sxs-lookup"><span data-stu-id="ddce5-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="ddce5-116">Örnek 3: belirtilen kaynak grubundaki tüm ımportexport işlerini listeler</span><span class="sxs-lookup"><span data-stu-id="ddce5-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ddce5-117">Bu cmdlet, belirtilen kaynak grubundaki tüm ımportexport işlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="ddce5-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="ddce5-118">Örnek 4: kimliğe göre ımportexport işini alma</span><span class="sxs-lookup"><span data-stu-id="ddce5-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ddce5-119">Bu cmdlet listeleri kimliğe göre ımportexport işini alır.</span><span class="sxs-lookup"><span data-stu-id="ddce5-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="ddce5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddce5-120">PARAMETERS</span></span>

### <span data-ttu-id="ddce5-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ddce5-121">-AcceptLanguage</span></span>
<span data-ttu-id="ddce5-122">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddce5-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="ddce5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddce5-123">-DefaultProfile</span></span>
<span data-ttu-id="ddce5-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddce5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddce5-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ddce5-125">-Filter</span></span>
<span data-ttu-id="ddce5-126">Sonuçları belirli koşullarla sınırlandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ddce5-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddce5-127">-InputObject</span></span>
<span data-ttu-id="ddce5-128">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddce5-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddce5-129">-Name</span></span>
<span data-ttu-id="ddce5-130">İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="ddce5-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddce5-131">-ResourceGroupName</span></span>
<span data-ttu-id="ddce5-132">Kaynak grubu adı, kullanıcı aboneliği içinde kaynak grubunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ddce5-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ddce5-133">-SubscriptionId</span></span>
<span data-ttu-id="ddce5-134">Azure kullanıcısına ait abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddce5-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-135">-Üst</span><span class="sxs-lookup"><span data-stu-id="ddce5-135">-Top</span></span>
<span data-ttu-id="ddce5-136">En çok kaç işin döndürüleceğini belirten bir tamsayı değeri.</span><span class="sxs-lookup"><span data-stu-id="ddce5-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="ddce5-137">Değer 100 ' ü aşamaz.</span><span class="sxs-lookup"><span data-stu-id="ddce5-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddce5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddce5-138">CommonParameters</span></span>
<span data-ttu-id="ddce5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddce5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddce5-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddce5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddce5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddce5-141">INPUTS</span></span>

### <span data-ttu-id="ddce5-142">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. ıımportexportidentity</span><span class="sxs-lookup"><span data-stu-id="ddce5-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="ddce5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddce5-143">OUTPUTS</span></span>

### <span data-ttu-id="ddce5-144">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101. ıjobresponse</span><span class="sxs-lookup"><span data-stu-id="ddce5-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="ddce5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddce5-145">NOTES</span></span>

<span data-ttu-id="ddce5-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ddce5-146">ALIASES</span></span>

<span data-ttu-id="ddce5-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ddce5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddce5-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ddce5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddce5-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddce5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddce5-150">INPUTOBJECT <IImportExportIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ddce5-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddce5-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ddce5-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddce5-152">`[JobName <String>]`: İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="ddce5-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="ddce5-153">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="ddce5-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="ddce5-154">Örneğin, Batı ABD veya westus.</span><span class="sxs-lookup"><span data-stu-id="ddce5-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="ddce5-155">`[ResourceGroupName <String>]`: Kaynak grubu adı, kaynak grubunu Kullanıcı aboneliğindeki benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ddce5-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="ddce5-156">`[SubscriptionId <String>]`: Azure kullanıcısının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddce5-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="ddce5-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddce5-157">RELATED LINKS</span></span>

