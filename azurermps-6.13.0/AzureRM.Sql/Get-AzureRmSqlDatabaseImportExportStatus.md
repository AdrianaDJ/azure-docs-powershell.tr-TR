---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: ad5e5bb73b3611c3c56c7340f740947134f72d39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587157"
---
# <span data-ttu-id="24711-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="24711-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="24711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24711-102">SYNOPSIS</span></span>
<span data-ttu-id="24711-103">Azure SQL veritabanı alma veya verme işleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="24711-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24711-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24711-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24711-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24711-105">DESCRIPTION</span></span>
<span data-ttu-id="24711-106">**Get-Azurermsqldatabaseımportexportstatus** cmdlet 'i, bir bacpac dosyasının ayrıntılarını bir depolama HESABıNDAN Azure SQL veritabanına aktarma ya da bır Azure SQL veritabanını bir geri.</span><span class="sxs-lookup"><span data-stu-id="24711-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="24711-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="24711-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="24711-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24711-108">EXAMPLES</span></span>

### <span data-ttu-id="24711-109">Örnek 1: SQL veritabanının içeri ve dışarı aktarma durumunu alma</span><span class="sxs-lookup"><span data-stu-id="24711-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="24711-110">Bu komut, belirtilen URL 'de bir veritabanı için içeri veya dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="24711-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="24711-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24711-111">PARAMETERS</span></span>

### <span data-ttu-id="24711-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24711-112">-DefaultProfile</span></span>
<span data-ttu-id="24711-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24711-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24711-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="24711-114">-OperationStatusLink</span></span>
<span data-ttu-id="24711-115">New-AzureRmSqlDatabaseExport veya New-AzureRmSqlDatabaseImport cmdlet 'lerinin döndürdüğü durum bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24711-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="24711-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="24711-116">-Confirm</span></span>
<span data-ttu-id="24711-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24711-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24711-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24711-118">-WhatIf</span></span>
<span data-ttu-id="24711-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24711-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24711-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24711-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24711-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24711-121">CommonParameters</span></span>
<span data-ttu-id="24711-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24711-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24711-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24711-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24711-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24711-124">INPUTS</span></span>

### <span data-ttu-id="24711-125">System. String</span><span class="sxs-lookup"><span data-stu-id="24711-125">System.String</span></span>

## <span data-ttu-id="24711-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24711-126">OUTPUTS</span></span>

### <span data-ttu-id="24711-127">Microsoft. Azure. Commands. Sql. ımportexport. model. Azurestabdatabaseımportexportstatusmodel</span><span class="sxs-lookup"><span data-stu-id="24711-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="24711-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24711-128">NOTES</span></span>
* <span data-ttu-id="24711-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="24711-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="24711-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24711-130">RELATED LINKS</span></span>

[<span data-ttu-id="24711-131">Yeni-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="24711-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="24711-132">Yeni-Azurermsqldatabaseımport</span><span class="sxs-lookup"><span data-stu-id="24711-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="24711-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="24711-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
