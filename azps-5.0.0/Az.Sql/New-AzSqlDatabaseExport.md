---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: c5b0295458d0efe443dc20ab069ccfb62a44eb49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276536"
---
# <span data-ttu-id="638bd-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="638bd-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="638bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638bd-102">SYNOPSIS</span></span>
<span data-ttu-id="638bd-103">Azure SQL veritabanını bir depolama hesabına. bacpac dosyası olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="638bd-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="638bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="638bd-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="638bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="638bd-105">DESCRIPTION</span></span>
<span data-ttu-id="638bd-106">**New-AzSqlDatabaseExport** cmdlet 'ı BIR Azure SQL veritabanını bir depolama hesabına. bacpac dosyası olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="638bd-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="638bd-107">Bu istek için durum bilgilerini almak üzere dışarı aktarma veritabanı durumunu Al isteği gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="638bd-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="638bd-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="638bd-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="638bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="638bd-109">EXAMPLES</span></span>

### <span data-ttu-id="638bd-110">Örnek 1: veritabanı için dışarı aktarma isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="638bd-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="638bd-111">Bu komut belirtilen veritabanı için dışarı aktarma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="638bd-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="638bd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="638bd-112">PARAMETERS</span></span>

### <span data-ttu-id="638bd-113">-\Administrators oturum açma</span><span class="sxs-lookup"><span data-stu-id="638bd-113">-AdministratorLogin</span></span>
<span data-ttu-id="638bd-114">SQL yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="638bd-115">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="638bd-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="638bd-116">SQL yöneticisinin parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="638bd-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="638bd-117">-AuthenticationType</span></span>
<span data-ttu-id="638bd-118">Sunucuya erişmek için kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="638bd-119">Varsayılan değer, kimlik doğrulama türü ayarlanmamışsa SQL olur.</span><span class="sxs-lookup"><span data-stu-id="638bd-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="638bd-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="638bd-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="638bd-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="638bd-121">Sql.</span></span>
<span data-ttu-id="638bd-122">SQL kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="638bd-122">SQL authentication.</span></span>
<span data-ttu-id="638bd-123">*\Administrators oturum açma* *ve yönetici* Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="638bd-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="638bd-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="638bd-124">ADPassword.</span></span>
<span data-ttu-id="638bd-125">Azure Active Directory kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="638bd-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="638bd-126">*\Administrators oturum açma* ve yöneticim *parolasını* Azure AD yöneticisi Kullanıcı adı ve parolasıyla ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="638bd-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="638bd-127">Bu parametre yalnızca SQL Veritabanı V12 sunucularında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="638bd-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="638bd-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="638bd-128">-DatabaseName</span></span>
<span data-ttu-id="638bd-129">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="638bd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638bd-130">-DefaultProfile</span></span>
<span data-ttu-id="638bd-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="638bd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="638bd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638bd-132">-ResourceGroupName</span></span>
<span data-ttu-id="638bd-133">SQL veritabanı sunucusu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="638bd-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="638bd-134">-ServerName</span></span>
<span data-ttu-id="638bd-135">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="638bd-136">-Sqlserverresourceıdforprivatelink</span><span class="sxs-lookup"><span data-stu-id="638bd-136">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="638bd-137">Özel bağlantı oluşturmak için SQL Server kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="638bd-137">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="638bd-138">-Storageaccountresourceıdforprivatelink</span><span class="sxs-lookup"><span data-stu-id="638bd-138">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="638bd-139">Özel bağlantı oluşturmak için depolama hesabı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="638bd-139">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="638bd-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="638bd-140">-StorageKey</span></span>
<span data-ttu-id="638bd-141">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-141">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="638bd-142">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="638bd-142">-StorageKeyType</span></span>
<span data-ttu-id="638bd-143">Depolama hesabının erişim anahtarı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-143">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="638bd-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="638bd-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="638bd-145">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="638bd-145">StorageAccessKey.</span></span>
<span data-ttu-id="638bd-146">Bu değer depolama hesabı anahtarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="638bd-146">This value uses a storage account key.</span></span> 
- <span data-ttu-id="638bd-147">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="638bd-147">SharedAccessKey.</span></span>
<span data-ttu-id="638bd-148">Bu değer, paylaşılan erişim Imzası (SAS) anahtarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="638bd-148">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="638bd-149">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="638bd-149">-StorageUri</span></span>
<span data-ttu-id="638bd-150">Blob bağlantısını URL olarak. bacpac dosyasına belirtir.</span><span class="sxs-lookup"><span data-stu-id="638bd-150">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="638bd-151">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="638bd-151">-UseNetworkIsolation</span></span>
<span data-ttu-id="638bd-152">Ayarlanırsa, depolama hesabı ve/veya SQL Server için özel bağlantı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="638bd-152">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="638bd-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="638bd-153">-Confirm</span></span>
<span data-ttu-id="638bd-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="638bd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="638bd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="638bd-155">-WhatIf</span></span>
<span data-ttu-id="638bd-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="638bd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="638bd-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="638bd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="638bd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638bd-158">CommonParameters</span></span>
<span data-ttu-id="638bd-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="638bd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638bd-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="638bd-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638bd-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="638bd-161">INPUTS</span></span>

### <span data-ttu-id="638bd-162">System. String</span><span class="sxs-lookup"><span data-stu-id="638bd-162">System.String</span></span>

## <span data-ttu-id="638bd-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="638bd-163">OUTPUTS</span></span>

### <span data-ttu-id="638bd-164">Microsoft. Azure. Commands. Sql. ımportexport. model. Azurestabdatabaseımportexportbasemodel</span><span class="sxs-lookup"><span data-stu-id="638bd-164">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="638bd-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="638bd-165">NOTES</span></span>
* <span data-ttu-id="638bd-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="638bd-166">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="638bd-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="638bd-167">RELATED LINKS</span></span>

[<span data-ttu-id="638bd-168">Get-Azsqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="638bd-168">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="638bd-169">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="638bd-169">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="638bd-170">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="638bd-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
