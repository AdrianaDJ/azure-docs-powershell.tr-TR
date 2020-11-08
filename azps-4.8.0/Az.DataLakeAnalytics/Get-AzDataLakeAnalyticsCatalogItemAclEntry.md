---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 134a236a8259a3197abed3b033c86904a9389643
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268309"
---
# <span data-ttu-id="9a150-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9a150-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="9a150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a150-102">SYNOPSIS</span></span>
<span data-ttu-id="9a150-103">Veri Lake Analytics 'teki bir kataloğun veya katalog öğesinin ACL 'sinin bir girişini alır.</span><span class="sxs-lookup"><span data-stu-id="9a150-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9a150-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a150-104">SYNTAX</span></span>

### <span data-ttu-id="9a150-105">GetCatalogAclEntry (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9a150-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a150-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="9a150-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a150-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="9a150-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a150-108">Getcatalogıtemaclentry</span><span class="sxs-lookup"><span data-stu-id="9a150-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a150-109">Getcatalogıtemaclentryforuserowner</span><span class="sxs-lookup"><span data-stu-id="9a150-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a150-110">Getcatalogıtemaclentryforgroupowner</span><span class="sxs-lookup"><span data-stu-id="9a150-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a150-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a150-111">DESCRIPTION</span></span>
<span data-ttu-id="9a150-112">**Get-Azdatalakeanalizleri Tic, Alogitemaclentry** cmdlet 'ı, Data Lake Analytics 'teki bir kataloğun veya katalog öğesinin erişim denetim LISTESINDEKI (ACL) girdi listesini (ACE) alır.</span><span class="sxs-lookup"><span data-stu-id="9a150-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9a150-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a150-113">EXAMPLES</span></span>

### <span data-ttu-id="9a150-114">Örnek 1: kataloğun ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="9a150-115">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9a150-116">Örnek 2: bir kataloğun Kullanıcı sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9a150-117">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun Kullanıcı sahibinin ACL girişini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9a150-118">Örnek 3: bir kataloğun grup sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9a150-119">Bu komut, belirtilen Data Lake Analytics hesabının kataloğunun grup sahibinin ACL girişini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9a150-120">Örnek 4: veritabanı ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="9a150-121">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9a150-122">Örnek 5: bir veritabanının kullanıcı sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9a150-123">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı için Kullanıcı sahibinin ACL girdisini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9a150-124">Örnek 6: bir veritabanının grup sahibinin ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9a150-125">Bu komut, belirtilen Data Lake Analytics hesabının veritabanı için Grup sahibinin ACL girdisini alır</span><span class="sxs-lookup"><span data-stu-id="9a150-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="9a150-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a150-126">PARAMETERS</span></span>

### <span data-ttu-id="9a150-127">-Hesap</span><span class="sxs-lookup"><span data-stu-id="9a150-127">-Account</span></span>
<span data-ttu-id="9a150-128">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a150-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9a150-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a150-129">-DefaultProfile</span></span>
<span data-ttu-id="9a150-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a150-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a150-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="9a150-131">-GroupOwner</span></span>
<span data-ttu-id="9a150-132">Grup sahibinin kataloğunun ACL girişini alma</span><span class="sxs-lookup"><span data-stu-id="9a150-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="9a150-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="9a150-133">-ItemType</span></span>
<span data-ttu-id="9a150-134">Kataloğun veya katalog öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a150-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="9a150-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9a150-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a150-136">Tan</span><span class="sxs-lookup"><span data-stu-id="9a150-136">Catalog</span></span>
- <span data-ttu-id="9a150-137">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="9a150-137">Database</span></span>

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

### <span data-ttu-id="9a150-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="9a150-138">-Path</span></span>
<span data-ttu-id="9a150-139">Katalog veya katalog öğesinin veri Lake Analytics yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a150-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="9a150-140">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="9a150-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="9a150-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="9a150-141">-UserOwner</span></span>
<span data-ttu-id="9a150-142">Kullanıcı sahibinin kataloğunun ACL girişini edinin.</span><span class="sxs-lookup"><span data-stu-id="9a150-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="9a150-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a150-143">CommonParameters</span></span>
<span data-ttu-id="9a150-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a150-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a150-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a150-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a150-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a150-146">INPUTS</span></span>

### <span data-ttu-id="9a150-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9a150-147">System.String</span></span>

### <span data-ttu-id="9a150-148">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="9a150-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="9a150-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a150-149">OUTPUTS</span></span>

### <span data-ttu-id="9a150-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDatalakeanaliz Tic</span><span class="sxs-lookup"><span data-stu-id="9a150-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="9a150-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a150-151">NOTES</span></span>

## <span data-ttu-id="9a150-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a150-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a150-153">U-SQL artık veritabanı düzeyinde erişim denetimi öneriyor</span><span class="sxs-lookup"><span data-stu-id="9a150-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="9a150-154">Remove-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="9a150-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="9a150-155">Set-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="9a150-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
