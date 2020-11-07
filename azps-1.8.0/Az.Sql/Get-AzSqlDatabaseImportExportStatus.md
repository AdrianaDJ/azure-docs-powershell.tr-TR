---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: b8a8100c55e10969eeee1723fe22deddfe5764ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759025"
---
# <span data-ttu-id="42ce9-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="42ce9-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="42ce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="42ce9-103">Azure SQL veritabanı alma veya verme işleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="42ce9-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="42ce9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42ce9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ce9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="42ce9-106">**Get-Azsqldatabaseımportexportstatus** cmdlet 'i, depolama hesabındaki bir bacpac dosyasının ayrıntılarını, bir depolama hesabındaki BIR Azure SQL veritabanına aktarma</span><span class="sxs-lookup"><span data-stu-id="42ce9-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="42ce9-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="42ce9-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="42ce9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42ce9-108">EXAMPLES</span></span>

### <span data-ttu-id="42ce9-109">Örnek 1: SQL veritabanının içeri ve dışarı aktarma durumunu alma</span><span class="sxs-lookup"><span data-stu-id="42ce9-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="42ce9-110">Bu komut, belirtilen URL 'de bir veritabanı için içeri veya dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="42ce9-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="42ce9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42ce9-111">PARAMETERS</span></span>

### <span data-ttu-id="42ce9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ce9-112">-DefaultProfile</span></span>
<span data-ttu-id="42ce9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42ce9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42ce9-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="42ce9-114">-OperationStatusLink</span></span>
<span data-ttu-id="42ce9-115">New-AzSqlDatabaseExport veya New-AzSqlDatabaseImport cmdlet 'lerinin döndürdüğü durum bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42ce9-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="42ce9-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="42ce9-116">-Confirm</span></span>
<span data-ttu-id="42ce9-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42ce9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ce9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ce9-118">-WhatIf</span></span>
<span data-ttu-id="42ce9-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42ce9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ce9-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42ce9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ce9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ce9-121">CommonParameters</span></span>
<span data-ttu-id="42ce9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42ce9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ce9-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42ce9-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ce9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42ce9-124">INPUTS</span></span>

### <span data-ttu-id="42ce9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="42ce9-125">System.String</span></span>

## <span data-ttu-id="42ce9-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42ce9-126">OUTPUTS</span></span>

### <span data-ttu-id="42ce9-127">Microsoft. Azure. Commands. Sql. ımportexport. model. Azurestabdatabaseımportexportstatusmodel</span><span class="sxs-lookup"><span data-stu-id="42ce9-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="42ce9-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42ce9-128">NOTES</span></span>
* <span data-ttu-id="42ce9-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="42ce9-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="42ce9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42ce9-130">RELATED LINKS</span></span>

[<span data-ttu-id="42ce9-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="42ce9-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="42ce9-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="42ce9-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="42ce9-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="42ce9-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
