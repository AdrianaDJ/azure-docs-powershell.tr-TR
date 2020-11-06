---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589950"
---
# <span data-ttu-id="f192f-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f192f-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="f192f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f192f-102">SYNOPSIS</span></span>
<span data-ttu-id="f192f-103">. Bacpac dosyası alır ve sunucuda yeni bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f192f-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f192f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f192f-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f192f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f192f-105">DESCRIPTION</span></span>
<span data-ttu-id="f192f-106">**New-Azurermsqldatabaseımport** cmdlet 'ı bir Azure depolama hesabından yeni BIR Azure SQL veritabanına bir bacpac dosyası içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="f192f-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="f192f-107">Bu istek için durum bilgilerini almak üzere içeri aktarma veritabanı durumunu Al isteği gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="f192f-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="f192f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f192f-108">EXAMPLES</span></span>

### <span data-ttu-id="f192f-109">Örnek 1: bacpac dosyası için içeri aktarma isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="f192f-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="f192f-110">Bu komut,. bacpac 'yi yeni bir veritabanına aktarmak için içeri aktarma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f192f-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="f192f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f192f-111">PARAMETERS</span></span>

### <span data-ttu-id="f192f-112">-\Administrators oturum açma</span><span class="sxs-lookup"><span data-stu-id="f192f-112">-AdministratorLogin</span></span>
<span data-ttu-id="f192f-113">SQL yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-114">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="f192f-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f192f-115">SQL yöneticisinin parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f192f-116">-AuthenticationType</span></span>
<span data-ttu-id="f192f-117">Sunucuya erişmek için kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="f192f-118">Kimlik doğrulama türü ayarlanmamışsa, bu parametre varsayılan olarak SQL kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f192f-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="f192f-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f192f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f192f-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="f192f-120">SQL.</span></span>
<span data-ttu-id="f192f-121">SQL kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="f192f-121">SQL authentication.</span></span>
<span data-ttu-id="f192f-122">*\Administrators oturum açma* ve yöneticim parametrelerini SQL Yöneticisi Kullanıcı *adına ve parolasına* ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f192f-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="f192f-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="f192f-123">ADPassword.</span></span>
<span data-ttu-id="f192f-124">Azure Active Directory kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="f192f-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="f192f-125">Active Directory Yöneticisi Kullanıcı *adı ve parolası* *için yönetic*</span><span class="sxs-lookup"><span data-stu-id="f192f-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="f192f-126">Bu parametre yalnızca SQL Veritabanı V12 sunucularında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f192f-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f192f-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="f192f-128">Yeni içeri aktarılan veritabanının boyut üst sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f192f-129">-DatabaseName</span></span>
<span data-ttu-id="f192f-130">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="f192f-131">-Edition</span></span>
<span data-ttu-id="f192f-132">İçeri aktarılacak yeni veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="f192f-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f192f-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f192f-134">Min</span><span class="sxs-lookup"><span data-stu-id="f192f-134">Premium</span></span>
- <span data-ttu-id="f192f-135">Ana</span><span class="sxs-lookup"><span data-stu-id="f192f-135">Basic</span></span>
- <span data-ttu-id="f192f-136">Ardından</span><span class="sxs-lookup"><span data-stu-id="f192f-136">Standard</span></span>
- <span data-ttu-id="f192f-137">Ambarı</span><span class="sxs-lookup"><span data-stu-id="f192f-137">DataWarehouse</span></span>
- <span data-ttu-id="f192f-138">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="f192f-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f192f-139">-ResourceGroupName</span></span>
<span data-ttu-id="f192f-140">SQL veritabanı sunucusu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-140">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f192f-141">-ServerName</span></span>
<span data-ttu-id="f192f-142">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-142">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f192f-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="f192f-144">Azure SQL veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f192f-145">-StorageKey</span></span>
<span data-ttu-id="f192f-146">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-146">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f192f-147">-StorageKeyType</span></span>
<span data-ttu-id="f192f-148">Depolama hesabının erişim anahtarı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="f192f-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f192f-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f192f-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f192f-150">StorageAccessKey.</span></span>
<span data-ttu-id="f192f-151">Depolama hesabı anahtarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="f192f-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="f192f-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f192f-152">SharedAccessKey.</span></span>
<span data-ttu-id="f192f-153">Paylaşılan erişim Imzasını (SAS) kullanır.</span><span class="sxs-lookup"><span data-stu-id="f192f-153">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases: 
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f192f-154">-StorageUri</span></span>
<span data-ttu-id="f192f-155">. Bacpac dosyasının blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f192f-155">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="f192f-156">-Confirm</span></span>
<span data-ttu-id="f192f-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f192f-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f192f-158">-WhatIf</span></span>
<span data-ttu-id="f192f-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f192f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f192f-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f192f-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f192f-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f192f-161">-DefaultProfile</span></span>
<span data-ttu-id="f192f-162">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f192f-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f192f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f192f-163">CommonParameters</span></span>
<span data-ttu-id="f192f-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f192f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f192f-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f192f-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f192f-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f192f-166">INPUTS</span></span>

## <span data-ttu-id="f192f-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f192f-167">OUTPUTS</span></span>

### <span data-ttu-id="f192f-168">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabaseımportexportbasemodel</span><span class="sxs-lookup"><span data-stu-id="f192f-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="f192f-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f192f-169">NOTES</span></span>
* <span data-ttu-id="f192f-170">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f192f-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f192f-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f192f-171">RELATED LINKS</span></span>

[<span data-ttu-id="f192f-172">Get-Azurermsqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="f192f-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f192f-173">Yeni-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f192f-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="f192f-174">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f192f-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

