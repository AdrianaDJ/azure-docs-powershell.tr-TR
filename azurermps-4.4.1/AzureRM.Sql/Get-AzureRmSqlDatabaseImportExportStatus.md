---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 5516556553931f7333e007edc6de1b4bd23b288d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762396"
---
# <span data-ttu-id="dde92-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="dde92-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="dde92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde92-102">SYNOPSIS</span></span>
<span data-ttu-id="dde92-103">Azure SQL veritabanı alma veya verme işleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dde92-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dde92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dde92-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde92-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dde92-105">DESCRIPTION</span></span>
<span data-ttu-id="dde92-106">**Get-Azurermsqldatabaseımportexportstatus** cmdlet 'i, bir bacpac dosyasının ayrıntılarını bir depolama HESABıNDAN Azure SQL veritabanına aktarma ya da bır Azure SQL veritabanını bir geri.</span><span class="sxs-lookup"><span data-stu-id="dde92-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="dde92-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="dde92-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="dde92-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dde92-108">EXAMPLES</span></span>

### <span data-ttu-id="dde92-109">Örnek 1: SQL veritabanının içeri ve dışarı aktarma durumunu alma</span><span class="sxs-lookup"><span data-stu-id="dde92-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="dde92-110">Bu komut, belirtilen URL 'de bir veritabanı için içeri veya dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="dde92-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="dde92-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dde92-111">PARAMETERS</span></span>

### <span data-ttu-id="dde92-112">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="dde92-112">-OperationStatusLink</span></span>
<span data-ttu-id="dde92-113">New-AzureRmSqlDatabaseExport veya New-AzureRmSqlDatabaseImport cmdlet 'lerinin döndürdüğü durum bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dde92-113">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="dde92-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="dde92-114">-Confirm</span></span>
<span data-ttu-id="dde92-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dde92-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde92-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde92-116">-WhatIf</span></span>
<span data-ttu-id="dde92-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dde92-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde92-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dde92-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde92-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde92-119">-DefaultProfile</span></span>
<span data-ttu-id="dde92-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dde92-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde92-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde92-121">CommonParameters</span></span>
<span data-ttu-id="dde92-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dde92-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde92-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde92-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde92-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dde92-124">INPUTS</span></span>

## <span data-ttu-id="dde92-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dde92-125">OUTPUTS</span></span>

## <span data-ttu-id="dde92-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dde92-126">NOTES</span></span>
* <span data-ttu-id="dde92-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="dde92-127">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dde92-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dde92-128">RELATED LINKS</span></span>

[<span data-ttu-id="dde92-129">Yeni-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="dde92-129">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="dde92-130">Yeni-Azurermsqldatabaseımport</span><span class="sxs-lookup"><span data-stu-id="dde92-130">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="dde92-131">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="dde92-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
