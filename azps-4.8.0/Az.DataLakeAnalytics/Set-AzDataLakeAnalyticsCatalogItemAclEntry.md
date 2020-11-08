---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275034"
---
# <span data-ttu-id="2813e-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2813e-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="2813e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2813e-102">SYNOPSIS</span></span>
<span data-ttu-id="2813e-103">Veri Lake Analytics 'teki katalog veya katalog öğesinin ACL 'SI içindeki girdiyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2813e-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="2813e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2813e-104">SYNTAX</span></span>

### <span data-ttu-id="2813e-105">SetCatalogAclEntryForUser (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2813e-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2813e-106">Setcatalogıtemaclentryforuser</span><span class="sxs-lookup"><span data-stu-id="2813e-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="2813e-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2813e-108">Setcatalogıtemaclentryforgroup</span><span class="sxs-lookup"><span data-stu-id="2813e-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="2813e-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-110">Setcatalogıtemaclentryforother</span><span class="sxs-lookup"><span data-stu-id="2813e-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="2813e-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-112">Setcatalogıtemaclentryforuserowner</span><span class="sxs-lookup"><span data-stu-id="2813e-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="2813e-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2813e-114">Setcatalogıtemaclentryforgroupowner</span><span class="sxs-lookup"><span data-stu-id="2813e-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2813e-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="2813e-115">DESCRIPTION</span></span>
<span data-ttu-id="2813e-116">**Set-Azdatalakeanalizleri Tic, Alogitemaclentry** cmdlet 'ı, Data Lake Analytics 'teki bir kataloğun veya katalog öğesinin erişim denetim lıstesıne (ACL) GIRDI (ACE) ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2813e-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="2813e-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2813e-117">EXAMPLES</span></span>

### <span data-ttu-id="2813e-118">Örnek 1: Katalog için Kullanıcı izinlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="2813e-119">Bu komut, Patti Tamlaştırıcı 'ın Katalog ACE 'sini okuma izinlerine sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2813e-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="2813e-120">Örnek 2: veritabanı için Kullanıcı Izinlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="2813e-121">Bu komut, Patti Tamleri'nin veritabanı ACE 'sini okuma izinlerine sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2813e-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="2813e-122">Örnek 3: kataloğun diğer izinlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="2813e-123">Bu komut, diğer için Katalog ACE 'sini okuma izinlerine sahip olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2813e-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="2813e-124">Örnek 4: veritabanı için diğer Izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="2813e-125">Örnek 5: kataloğun Kullanıcı sahibi izinlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="2813e-126">Bu komut, hesabın sahip iznini okuma izni olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2813e-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="2813e-127">Örnek 6: veritabanı için Kullanıcı sahibi Izinlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2813e-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="2813e-128">Bu komut, veritabanının sahip iznini okuma izni olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2813e-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="2813e-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2813e-129">PARAMETERS</span></span>

### <span data-ttu-id="2813e-130">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2813e-130">-Account</span></span>
<span data-ttu-id="2813e-131">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2813e-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2813e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2813e-132">-DefaultProfile</span></span>
<span data-ttu-id="2813e-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2813e-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2813e-134">-Group</span><span class="sxs-lookup"><span data-stu-id="2813e-134">-Group</span></span>
<span data-ttu-id="2813e-135">Grubun kataloğunun ACL girişini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2813e-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="2813e-136">-GroupOwner</span></span>
<span data-ttu-id="2813e-137">Grup sahibinin kataloğunun ACL girişini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2813e-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2813e-138">-ItemType</span></span>
<span data-ttu-id="2813e-139">Kataloğun veya katalog öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2813e-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="2813e-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2813e-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2813e-141">Tan</span><span class="sxs-lookup"><span data-stu-id="2813e-141">Catalog</span></span>
- <span data-ttu-id="2813e-142">Veritabanı</span><span class="sxs-lookup"><span data-stu-id="2813e-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-143">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="2813e-143">-ObjectId</span></span>
<span data-ttu-id="2813e-144">Ayarlanacak kullanıcının kimliği.</span><span class="sxs-lookup"><span data-stu-id="2813e-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-145">-Diğer</span><span class="sxs-lookup"><span data-stu-id="2813e-145">-Other</span></span>
<span data-ttu-id="2813e-146">Kataloğun ACL girişini başka bir şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2813e-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-147">-Yol</span><span class="sxs-lookup"><span data-stu-id="2813e-147">-Path</span></span>
<span data-ttu-id="2813e-148">Katalog veya katalog öğesinin veri Lake Analytics yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2813e-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="2813e-149">Yolun bölümleri noktayla ayrılmalıdır (.).</span><span class="sxs-lookup"><span data-stu-id="2813e-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-150">-İzinler</span><span class="sxs-lookup"><span data-stu-id="2813e-150">-Permissions</span></span>
<span data-ttu-id="2813e-151">ACE izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2813e-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="2813e-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2813e-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2813e-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2813e-153">None</span></span>
- <span data-ttu-id="2813e-154">Okuması</span><span class="sxs-lookup"><span data-stu-id="2813e-154">Read</span></span>
- <span data-ttu-id="2813e-155">Yazma</span><span class="sxs-lookup"><span data-stu-id="2813e-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-156">-Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="2813e-156">-User</span></span>
<span data-ttu-id="2813e-157">Kullanıcı için kataloğun ACL girişini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2813e-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="2813e-158">-UserOwner</span></span>
<span data-ttu-id="2813e-159">Kullanıcının sahibi için kataloğun ACL girişini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2813e-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2813e-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="2813e-160">-Confirm</span></span>
<span data-ttu-id="2813e-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2813e-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2813e-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2813e-162">-WhatIf</span></span>
<span data-ttu-id="2813e-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2813e-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2813e-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2813e-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2813e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2813e-165">CommonParameters</span></span>
<span data-ttu-id="2813e-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2813e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2813e-167">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2813e-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2813e-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2813e-168">INPUTS</span></span>

### <span data-ttu-id="2813e-169">System. String</span><span class="sxs-lookup"><span data-stu-id="2813e-169">System.String</span></span>

### <span data-ttu-id="2813e-170">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2813e-170">System.Guid</span></span>

### <span data-ttu-id="2813e-171">Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance</span><span class="sxs-lookup"><span data-stu-id="2813e-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="2813e-172">Microsoft. Azure. Commands. datalakeanalytics. model</span><span class="sxs-lookup"><span data-stu-id="2813e-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="2813e-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2813e-173">OUTPUTS</span></span>

### <span data-ttu-id="2813e-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDatalakeanaliz Tic</span><span class="sxs-lookup"><span data-stu-id="2813e-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="2813e-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2813e-175">NOTES</span></span>

## <span data-ttu-id="2813e-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2813e-176">RELATED LINKS</span></span>

[<span data-ttu-id="2813e-177">Get-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="2813e-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="2813e-178">Remove-azdatalakeanalyzer ticdağı</span><span class="sxs-lookup"><span data-stu-id="2813e-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="2813e-179">U-SQL artık veritabanı düzeyinde erişim denetimi öneriyor</span><span class="sxs-lookup"><span data-stu-id="2813e-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
