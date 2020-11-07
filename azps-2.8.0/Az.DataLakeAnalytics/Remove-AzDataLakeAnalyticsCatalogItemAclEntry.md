---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 6d30985baed220ee4a7a599f1214c0c4124ef08d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752383"
---
# <span data-ttu-id="24cfa-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="24cfa-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="24cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="24cfa-103">Veri Lake Analytics 'teki bir kataloğun veya katalog öğesinin ACL 'sinden girdi siler.</span><span class="sxs-lookup"><span data-stu-id="24cfa-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="24cfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24cfa-104">SYNTAX</span></span>

### <span data-ttu-id="24cfa-105">RemoveCatalogAclEntryForUser (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24cfa-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cfa-106">Removecatalogıtemaclentryforuser</span><span class="sxs-lookup"><span data-stu-id="24cfa-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24cfa-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="24cfa-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cfa-108">Removecatalogıtemaclentryforgroup</span><span class="sxs-lookup"><span data-stu-id="24cfa-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24cfa-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="24cfa-109">DESCRIPTION</span></span>
<span data-ttu-id="24cfa-110">**Remove-Azdatalakeanalizleri Tic, Alogitemaclentry** cmdlet 'ı, Data Lake Analytics 'teki bir kataloğun veya katalog öğesinin erişim denetim LISTESINDEN (ACL) bir GIRIŞINI (ACE) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24cfa-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="24cfa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24cfa-111">EXAMPLES</span></span>

### <span data-ttu-id="24cfa-112">Örnek 1: kataloğun Kullanıcı ACL 'sini kaldırma</span><span class="sxs-lookup"><span data-stu-id="24cfa-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="24cfa-113">Bu komut, contosoadla hesabının PATTI Fuller için Katalog ACL 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24cfa-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="24cfa-114">Örnek 2: veritabanının kullanıcı ACL 'sini kaldırma</span><span class="sxs-lookup"><span data-stu-id="24cfa-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="24cfa-115">Bu komut, contosoadla hesabının PATTI Tamlaştırıcı veritabanı ACL 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="24cfa-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="24cfa-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24cfa-116">PARAMETERS</span></span>

### <span data-ttu-id="24cfa-117">-Hesap</span><span class="sxs-lookup"><span data-stu-id="24cfa-117">-Account</span></span>
<span data-ttu-id="24cfa-118">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24cfa-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="24cfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cfa-119">-DefaultProfile</span></span>
<span data-ttu-id="24cfa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24cfa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cfa-121">-Group</span><span class="sxs-lookup"><span data-stu-id="24cfa-121">-Group</span></span>
<span data-ttu-id="24cfa-122">Grubun kataloğunun ACL girişini kaldır.</span><span class="sxs-lookup"><span data-stu-id="24cfa-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cfa-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="24cfa-123">-ItemType</span></span>
<span data-ttu-id="24cfa-124">Kataloğun veya katalog öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="24cfa-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="24cfa-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="24cfa-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="24cfa-126">Tan</span><span class="sxs-lookup"><span data-stu-id="24cfa-126">Catalog</span></span>
- <span data-ttu-id="24cfa-127">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="24cfa-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cfa-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="24cfa-128">-ObjectId</span></span>
<span data-ttu-id="24cfa-129">Kaldırılacak kullanıcının kimliği.</span><span class="sxs-lookup"><span data-stu-id="24cfa-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cfa-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="24cfa-130">-PassThru</span></span>
<span data-ttu-id="24cfa-131">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24cfa-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="24cfa-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="24cfa-132">-Path</span></span>
<span data-ttu-id="24cfa-133">Katalog veya katalog öğesinin veri Lake Analytics yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="24cfa-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="24cfa-134">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="24cfa-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cfa-135">-Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="24cfa-135">-User</span></span>
<span data-ttu-id="24cfa-136">Kullanıcı için kataloğun ACL girişini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="24cfa-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cfa-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="24cfa-137">-Confirm</span></span>
<span data-ttu-id="24cfa-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24cfa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cfa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cfa-139">-WhatIf</span></span>
<span data-ttu-id="24cfa-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24cfa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cfa-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24cfa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cfa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cfa-142">CommonParameters</span></span>
<span data-ttu-id="24cfa-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24cfa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cfa-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cfa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cfa-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24cfa-145">INPUTS</span></span>

### <span data-ttu-id="24cfa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="24cfa-146">System.String</span></span>

### <span data-ttu-id="24cfa-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="24cfa-147">System.Guid</span></span>

### <span data-ttu-id="24cfa-148">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="24cfa-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="24cfa-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24cfa-149">OUTPUTS</span></span>

### <span data-ttu-id="24cfa-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24cfa-150">System.Boolean</span></span>

## <span data-ttu-id="24cfa-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24cfa-151">NOTES</span></span>

## <span data-ttu-id="24cfa-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24cfa-152">RELATED LINKS</span></span>

[<span data-ttu-id="24cfa-153">U-SQL artık veritabanı düzeyinde erişim denetimi öneriyor</span><span class="sxs-lookup"><span data-stu-id="24cfa-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="24cfa-154">Get-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="24cfa-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="24cfa-155">Set-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="24cfa-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
