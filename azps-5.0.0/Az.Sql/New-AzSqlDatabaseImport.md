---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 074261adf9c2f5501ca12753971fac08783ab36f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325444"
---
# <span data-ttu-id="38f4f-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="38f4f-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="38f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="38f4f-103">. Bacpac dosyası alır ve sunucuda yeni bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38f4f-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="38f4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38f4f-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38f4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="38f4f-106">**New-Azsqldatabaseımport** cmdlet 'ı bir Azure depolama hesabından yeni BIR Azure SQL veritabanına bir bacpac dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="38f4f-107">Bu istek için durum bilgilerini almak üzere içeri aktarma veritabanı durumunu Al isteği gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="38f4f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38f4f-108">EXAMPLES</span></span>

### <span data-ttu-id="38f4f-109">Örnek 1: bacpac dosyası için içeri aktarma isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="38f4f-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="38f4f-110">Bu komut,. bacpac 'yi yeni bir veritabanına aktarmak için içeri aktarma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38f4f-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="38f4f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38f4f-111">PARAMETERS</span></span>

### <span data-ttu-id="38f4f-112">-\Administrators oturum açma</span><span class="sxs-lookup"><span data-stu-id="38f4f-112">-AdministratorLogin</span></span>
<span data-ttu-id="38f4f-113">SQL yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="38f4f-114">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="38f4f-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="38f4f-115">SQL yöneticisinin parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="38f4f-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="38f4f-116">-AuthenticationType</span></span>
<span data-ttu-id="38f4f-117">Sunucuya erişmek için kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="38f4f-118">Kimlik doğrulama türü ayarlanmamışsa, bu parametre varsayılan olarak SQL kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="38f4f-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="38f4f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38f4f-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="38f4f-120">SQL.</span></span>
<span data-ttu-id="38f4f-121">SQL kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="38f4f-121">SQL authentication.</span></span>
<span data-ttu-id="38f4f-122">*\Administrators oturum açma* ve yöneticim parametrelerini SQL Yöneticisi Kullanıcı *adına ve parolasına* ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="38f4f-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="38f4f-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="38f4f-123">ADPassword.</span></span>
<span data-ttu-id="38f4f-124">Azure Active Directory kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="38f4f-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="38f4f-125">Active Directory Yöneticisi Kullanıcı *adı ve parolası* *için yönetic*</span><span class="sxs-lookup"><span data-stu-id="38f4f-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="38f4f-126">Bu parametre yalnızca SQL Veritabanı V12 sunucularında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="38f4f-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="38f4f-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="38f4f-128">Yeni içeri aktarılan veritabanının boyut üst sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="38f4f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38f4f-129">-DatabaseName</span></span>
<span data-ttu-id="38f4f-130">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="38f4f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f4f-131">-DefaultProfile</span></span>
<span data-ttu-id="38f4f-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="38f4f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38f4f-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="38f4f-133">-Edition</span></span>
<span data-ttu-id="38f4f-134">İçeri aktarılacak yeni veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="38f4f-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="38f4f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38f4f-136">Min</span><span class="sxs-lookup"><span data-stu-id="38f4f-136">Premium</span></span>
- <span data-ttu-id="38f4f-137">Ana</span><span class="sxs-lookup"><span data-stu-id="38f4f-137">Basic</span></span>
- <span data-ttu-id="38f4f-138">Ardından</span><span class="sxs-lookup"><span data-stu-id="38f4f-138">Standard</span></span>
- <span data-ttu-id="38f4f-139">Ambarı</span><span class="sxs-lookup"><span data-stu-id="38f4f-139">DataWarehouse</span></span>
- <span data-ttu-id="38f4f-140">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="38f4f-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f4f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f4f-141">-ResourceGroupName</span></span>
<span data-ttu-id="38f4f-142">SQL veritabanı sunucusu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="38f4f-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38f4f-143">-ServerName</span></span>
<span data-ttu-id="38f4f-144">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="38f4f-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="38f4f-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="38f4f-146">Azure SQL veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="38f4f-147">-Sqlserverresourceıdforprivatelink</span><span class="sxs-lookup"><span data-stu-id="38f4f-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="38f4f-148">Özel bağlantı oluşturmak için SQL Server kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="38f4f-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="38f4f-149">-Storageaccountresourceıdforprivatelink</span><span class="sxs-lookup"><span data-stu-id="38f4f-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="38f4f-150">Özel bağlantı oluşturmak için depolama hesabı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="38f4f-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="38f4f-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="38f4f-151">-StorageKey</span></span>
<span data-ttu-id="38f4f-152">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="38f4f-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="38f4f-153">-StorageKeyType</span></span>
<span data-ttu-id="38f4f-154">Depolama hesabının erişim anahtarı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="38f4f-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="38f4f-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38f4f-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="38f4f-156">StorageAccessKey.</span></span>
<span data-ttu-id="38f4f-157">Depolama hesabı anahtarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="38f4f-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="38f4f-158">SharedAccessKey.</span></span>
<span data-ttu-id="38f4f-159">Paylaşılan erişim Imzasını (SAS) kullanır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="38f4f-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="38f4f-160">-StorageUri</span></span>
<span data-ttu-id="38f4f-161">. Bacpac dosyasının blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="38f4f-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="38f4f-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="38f4f-163">Ayarlanırsa, depolama hesabı ve/veya SQL Server için özel bağlantı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="38f4f-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f4f-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="38f4f-164">-Confirm</span></span>
<span data-ttu-id="38f4f-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38f4f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f4f-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f4f-166">-WhatIf</span></span>
<span data-ttu-id="38f4f-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f4f-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38f4f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f4f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f4f-169">CommonParameters</span></span>
<span data-ttu-id="38f4f-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38f4f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f4f-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="38f4f-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f4f-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38f4f-172">INPUTS</span></span>

### <span data-ttu-id="38f4f-173">System. String</span><span class="sxs-lookup"><span data-stu-id="38f4f-173">System.String</span></span>

## <span data-ttu-id="38f4f-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38f4f-174">OUTPUTS</span></span>

### <span data-ttu-id="38f4f-175">Microsoft. Azure. Commands. Sql. ımportexport. model. Azurestabdatabaseımportexportbasemodel</span><span class="sxs-lookup"><span data-stu-id="38f4f-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="38f4f-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38f4f-176">NOTES</span></span>
* <span data-ttu-id="38f4f-177">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="38f4f-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="38f4f-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38f4f-178">RELATED LINKS</span></span>

[<span data-ttu-id="38f4f-179">Get-Azsqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="38f4f-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="38f4f-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="38f4f-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="38f4f-181">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

