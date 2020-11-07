---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 838c09c8a86c081a1b335fa22f4473d099a1b182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764102"
---
# <span data-ttu-id="16148-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="16148-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="16148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16148-102">SYNOPSIS</span></span>
<span data-ttu-id="16148-103">Azure SQL veritabanını bir depolama hesabına. bacpac dosyası olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="16148-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16148-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16148-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16148-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16148-105">DESCRIPTION</span></span>
<span data-ttu-id="16148-106">**New-AzureRmSqlDatabaseExport** cmdlet 'ı BIR Azure SQL veritabanını bir depolama hesabına. bacpac dosyası olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="16148-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="16148-107">Bu istek için durum bilgilerini almak üzere dışarı aktarma veritabanı durumunu Al isteği gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="16148-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="16148-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="16148-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="16148-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16148-109">EXAMPLES</span></span>

### <span data-ttu-id="16148-110">Örnek 1: veritabanı için dışarı aktarma isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="16148-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="16148-111">Bu komut belirtilen veritabanı için dışarı aktarma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16148-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="16148-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16148-112">PARAMETERS</span></span>

### <span data-ttu-id="16148-113">-\Administrators oturum açma</span><span class="sxs-lookup"><span data-stu-id="16148-113">-AdministratorLogin</span></span>
<span data-ttu-id="16148-114">SQL yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="16148-115">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="16148-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="16148-116">SQL yöneticisinin parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="16148-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="16148-117">-AuthenticationType</span></span>
<span data-ttu-id="16148-118">Sunucuya erişmek için kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="16148-119">Varsayılan değer, kimlik doğrulama türü ayarlanmamışsa SQL olur.</span><span class="sxs-lookup"><span data-stu-id="16148-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="16148-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="16148-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16148-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="16148-121">Sql.</span></span>
<span data-ttu-id="16148-122">SQL kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="16148-122">SQL authentication.</span></span>
<span data-ttu-id="16148-123">*\Administrators oturum açma* *ve yönetici* Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="16148-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="16148-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="16148-124">ADPassword.</span></span>
<span data-ttu-id="16148-125">Azure Active Directory kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="16148-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="16148-126">*\Administrators oturum açma* ve yöneticim *parolasını* Azure AD yöneticisi Kullanıcı adı ve parolasıyla ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16148-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="16148-127">Bu parametre yalnızca SQL Veritabanı V12 sunucularında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="16148-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="16148-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16148-128">-DatabaseName</span></span>
<span data-ttu-id="16148-129">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="16148-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16148-130">-DefaultProfile</span></span>
<span data-ttu-id="16148-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16148-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16148-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16148-132">-ResourceGroupName</span></span>
<span data-ttu-id="16148-133">SQL veritabanı sunucusu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="16148-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16148-134">-ServerName</span></span>
<span data-ttu-id="16148-135">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="16148-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="16148-136">-StorageKey</span></span>
<span data-ttu-id="16148-137">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="16148-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="16148-138">-StorageKeyType</span></span>
<span data-ttu-id="16148-139">Depolama hesabının erişim anahtarı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="16148-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="16148-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16148-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="16148-141">StorageAccessKey.</span></span>
<span data-ttu-id="16148-142">Bu değer depolama hesabı anahtarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="16148-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="16148-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="16148-143">SharedAccessKey.</span></span>
<span data-ttu-id="16148-144">Bu değer, paylaşılan erişim Imzası (SAS) anahtarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="16148-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="16148-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="16148-145">-StorageUri</span></span>
<span data-ttu-id="16148-146">Blob bağlantısını URL olarak. bacpac dosyasına belirtir.</span><span class="sxs-lookup"><span data-stu-id="16148-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="16148-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="16148-147">-Confirm</span></span>
<span data-ttu-id="16148-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16148-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16148-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16148-149">-WhatIf</span></span>
<span data-ttu-id="16148-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16148-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16148-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16148-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16148-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16148-152">CommonParameters</span></span>
<span data-ttu-id="16148-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16148-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16148-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16148-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16148-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16148-155">INPUTS</span></span>

### <span data-ttu-id="16148-156">System. String</span><span class="sxs-lookup"><span data-stu-id="16148-156">System.String</span></span>

## <span data-ttu-id="16148-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16148-157">OUTPUTS</span></span>

### <span data-ttu-id="16148-158">Microsoft. Azure. Commands. Sql. ımportexport. model. Azurestabdatabaseımportexportbasemodel</span><span class="sxs-lookup"><span data-stu-id="16148-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="16148-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16148-159">NOTES</span></span>
* <span data-ttu-id="16148-160">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="16148-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="16148-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16148-161">RELATED LINKS</span></span>

[<span data-ttu-id="16148-162">Get-Azurermsqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="16148-162">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="16148-163">Yeni-Azurermsqldatabaseımport</span><span class="sxs-lookup"><span data-stu-id="16148-163">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="16148-164">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="16148-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
