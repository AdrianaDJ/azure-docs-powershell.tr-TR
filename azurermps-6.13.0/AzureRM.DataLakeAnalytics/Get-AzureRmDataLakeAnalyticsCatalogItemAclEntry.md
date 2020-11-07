---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763870"
---
# <span data-ttu-id="3fc13-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3fc13-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="3fc13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc13-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc13-103">Veri Lake Analytics 'teki bir kataloğun veya katalog öğesinin ACL 'sinin bir girişini alır.</span><span class="sxs-lookup"><span data-stu-id="3fc13-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fc13-104">SYNTAX</span></span>

### <span data-ttu-id="3fc13-105">GetCatalogAclEntry (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3fc13-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fc13-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="3fc13-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc13-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="3fc13-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc13-108">Getcatalogıtemaclentry</span><span class="sxs-lookup"><span data-stu-id="3fc13-108">GetCatalogItemAclEntry</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc13-109">Getcatalogıtemaclentryforuserowner</span><span class="sxs-lookup"><span data-stu-id="3fc13-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc13-110">Getcatalogıtemaclentryforgroupowner</span><span class="sxs-lookup"><span data-stu-id="3fc13-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc13-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fc13-111">DESCRIPTION</span></span>
<span data-ttu-id="3fc13-112">**Get-Azurermdatalakeanalizticdağıda** , Data Lake Analytics 'teki bir kataloğun veya katalog öğesinin erişim denetim LISTESINDEKI (ACL) girdilerin (ACE) listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3fc13-112">The **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="3fc13-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fc13-113">EXAMPLES</span></span>

### <span data-ttu-id="3fc13-114">Örnek 1: kataloğun ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="3fc13-115">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3fc13-116">Örnek 2: bir kataloğun Kullanıcı sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3fc13-117">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun Kullanıcı sahibinin ACL girişini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3fc13-118">Örnek 3: bir kataloğun grup sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3fc13-119">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun grup sahibinin ACL girişini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3fc13-120">Örnek 4: veritabanı ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="3fc13-121">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3fc13-122">Örnek 5: bir veritabanının kullanıcı sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3fc13-123">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı için Kullanıcı sahibinin ACL girdisini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3fc13-124">Örnek 6: bir veritabanının grup sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3fc13-125">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı için Grup sahibinin ACL girdisini alır</span><span class="sxs-lookup"><span data-stu-id="3fc13-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="3fc13-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fc13-126">PARAMETERS</span></span>

### <span data-ttu-id="3fc13-127">-Hesap</span><span class="sxs-lookup"><span data-stu-id="3fc13-127">-Account</span></span>
<span data-ttu-id="3fc13-128">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fc13-128">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc13-129">-DefaultProfile</span></span>
<span data-ttu-id="3fc13-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fc13-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="3fc13-131">-GroupOwner</span></span>
<span data-ttu-id="3fc13-132">Grup sahibinin kataloğunun ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="3fc13-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="3fc13-133">-ItemType</span></span>
<span data-ttu-id="3fc13-134">Kataloğun veya katalog öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fc13-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="3fc13-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3fc13-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3fc13-136">Tan</span><span class="sxs-lookup"><span data-stu-id="3fc13-136">Catalog</span></span>
- <span data-ttu-id="3fc13-137">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="3fc13-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="3fc13-138">-Path</span></span>
<span data-ttu-id="3fc13-139">Katalog veya katalog öğesinin veri Lake Analytics yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fc13-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="3fc13-140">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="3fc13-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="3fc13-141">-UserOwner</span></span>
<span data-ttu-id="3fc13-142">Kullanıcı sahibinin kataloğunun ACL girişini edinin.</span><span class="sxs-lookup"><span data-stu-id="3fc13-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc13-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc13-143">CommonParameters</span></span>
<span data-ttu-id="3fc13-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fc13-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc13-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc13-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc13-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fc13-146">INPUTS</span></span>

### <span data-ttu-id="3fc13-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3fc13-147">System.String</span></span>

### <span data-ttu-id="3fc13-148">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="3fc13-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="3fc13-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fc13-149">OUTPUTS</span></span>

### <span data-ttu-id="3fc13-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDatalakeanaliz Tic</span><span class="sxs-lookup"><span data-stu-id="3fc13-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="3fc13-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fc13-151">NOTES</span></span>

## <span data-ttu-id="3fc13-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fc13-152">RELATED LINKS</span></span>

[<span data-ttu-id="3fc13-153">U-SQL artık veritabanı düzeyinde erişim denetimi öneriyor</span><span class="sxs-lookup"><span data-stu-id="3fc13-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="3fc13-154">Remove-Azurermdatalakeanalyzer Tic, Alogıtemacmactry</span><span class="sxs-lookup"><span data-stu-id="3fc13-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="3fc13-155">Set-Azurermdatalakeanalyzer Ticwidealogıtemactry</span><span class="sxs-lookup"><span data-stu-id="3fc13-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
