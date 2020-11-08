---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268227"
---
# <span data-ttu-id="83e0f-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="83e0f-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="83e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="83e0f-103">İçeri veya dışarı aktarma işiyle ilişkili diskleri sevk ettiğiniz bir konum hakkındaki ayrıntıları verir.</span><span class="sxs-lookup"><span data-stu-id="83e0f-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="83e0f-104">Konum bir Azure bölgedir.</span><span class="sxs-lookup"><span data-stu-id="83e0f-104">A location is an Azure region.</span></span>

## <span data-ttu-id="83e0f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83e0f-105">SYNTAX</span></span>

### <span data-ttu-id="83e0f-106">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83e0f-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83e0f-107">Al</span><span class="sxs-lookup"><span data-stu-id="83e0f-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83e0f-108">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="83e0f-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83e0f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="83e0f-109">DESCRIPTION</span></span>
<span data-ttu-id="83e0f-110">İçeri veya dışarı aktarma işiyle ilişkili diskleri sevk ettiğiniz bir konum hakkındaki ayrıntıları verir.</span><span class="sxs-lookup"><span data-stu-id="83e0f-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="83e0f-111">Konum bir Azure bölgedir.</span><span class="sxs-lookup"><span data-stu-id="83e0f-111">A location is an Azure region.</span></span>

## <span data-ttu-id="83e0f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83e0f-112">EXAMPLES</span></span>

### <span data-ttu-id="83e0f-113">Örnek 1: varsayılan içerikle tüm Azure bölge konumu ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="83e0f-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="83e0f-114">Bu cmdlet, tüm Azure bölge konumu ayrıntılarını varsayılan içerikle alır.</span><span class="sxs-lookup"><span data-stu-id="83e0f-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="83e0f-115">Örnek 2: konum adına göre Azure bölgesi konum ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="83e0f-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="83e0f-116">Bu cmdlet, Azure bölgesi konum ayrıntılarını konum adına göre alır.</span><span class="sxs-lookup"><span data-stu-id="83e0f-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="83e0f-117">Örnek 3: kimliğe göre Azure bölge konumu ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="83e0f-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="83e0f-118">Bu cmdlet listeleri, Azure bölgesi konum ayrıntılarını kimlik olarak alır.</span><span class="sxs-lookup"><span data-stu-id="83e0f-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="83e0f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83e0f-119">PARAMETERS</span></span>

### <span data-ttu-id="83e0f-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="83e0f-120">-AcceptLanguage</span></span>
<span data-ttu-id="83e0f-121">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="83e0f-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="83e0f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e0f-122">-DefaultProfile</span></span>
<span data-ttu-id="83e0f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83e0f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e0f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83e0f-124">-InputObject</span></span>
<span data-ttu-id="83e0f-125">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83e0f-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83e0f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="83e0f-126">-Name</span></span>
<span data-ttu-id="83e0f-127">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="83e0f-127">The name of the location.</span></span>
<span data-ttu-id="83e0f-128">Örneğin, Batı ABD veya westus.</span><span class="sxs-lookup"><span data-stu-id="83e0f-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e0f-129">CommonParameters</span></span>
<span data-ttu-id="83e0f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83e0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e0f-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83e0f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e0f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83e0f-132">INPUTS</span></span>

### <span data-ttu-id="83e0f-133">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. ıımportexportidentity</span><span class="sxs-lookup"><span data-stu-id="83e0f-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="83e0f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83e0f-134">OUTPUTS</span></span>

### <span data-ttu-id="83e0f-135">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101.</span><span class="sxs-lookup"><span data-stu-id="83e0f-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="83e0f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83e0f-136">NOTES</span></span>

<span data-ttu-id="83e0f-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="83e0f-137">ALIASES</span></span>

<span data-ttu-id="83e0f-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="83e0f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83e0f-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="83e0f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83e0f-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83e0f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83e0f-141">INPUTOBJECT <IImportExportIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="83e0f-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83e0f-142">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="83e0f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83e0f-143">`[JobName <String>]`: İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="83e0f-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="83e0f-144">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="83e0f-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="83e0f-145">Örneğin, Batı ABD veya westus.</span><span class="sxs-lookup"><span data-stu-id="83e0f-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="83e0f-146">`[ResourceGroupName <String>]`: Kaynak grubu adı, kaynak grubunu Kullanıcı aboneliğindeki benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="83e0f-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="83e0f-147">`[SubscriptionId <String>]`: Azure kullanıcısının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83e0f-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="83e0f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83e0f-148">RELATED LINKS</span></span>

