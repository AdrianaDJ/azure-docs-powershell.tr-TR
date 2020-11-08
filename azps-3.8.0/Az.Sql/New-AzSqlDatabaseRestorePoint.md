---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097947"
---
# <span data-ttu-id="59c84-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="59c84-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="59c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c84-102">SYNOPSIS</span></span>
<span data-ttu-id="59c84-103">SQL veritabanının geri yüklenebildiği yeni bir geri yükleme noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59c84-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="59c84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59c84-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59c84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59c84-105">DESCRIPTION</span></span>
<span data-ttu-id="59c84-106">**New-AzSqlDatabaseRestorePoint** cmdlet 'ı BIR Azure SQL veri ambarının geri yüklenebileceğini belirten yeni bir geri yükleme noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59c84-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="59c84-107">Bu cmdlet Şu anda Azure SQL veri ambarı için destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="59c84-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="59c84-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59c84-108">EXAMPLES</span></span>

### <span data-ttu-id="59c84-109">Örnek 1: geri yükleme noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="59c84-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="59c84-110">Bu komut, Azure SQL veri ambarı için geri yükleme noktası oluşturur ve geri yükleme noktasının ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="59c84-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="59c84-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59c84-111">PARAMETERS</span></span>

### <span data-ttu-id="59c84-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59c84-112">-DatabaseName</span></span>
<span data-ttu-id="59c84-113">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59c84-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="59c84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c84-114">-DefaultProfile</span></span>
<span data-ttu-id="59c84-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59c84-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59c84-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c84-116">-ResourceGroupName</span></span>
<span data-ttu-id="59c84-117">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59c84-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="59c84-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="59c84-118">-RestorePointLabel</span></span>
<span data-ttu-id="59c84-119">Kolay tanımlama için geri yükleme noktasının etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59c84-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c84-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59c84-120">-ServerName</span></span>
<span data-ttu-id="59c84-121">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59c84-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="59c84-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="59c84-122">-Confirm</span></span>
<span data-ttu-id="59c84-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59c84-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c84-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c84-124">-WhatIf</span></span>
<span data-ttu-id="59c84-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59c84-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c84-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59c84-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c84-127">CommonParameters</span></span>
<span data-ttu-id="59c84-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59c84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c84-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59c84-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c84-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59c84-130">INPUTS</span></span>

### <span data-ttu-id="59c84-131">System. String</span><span class="sxs-lookup"><span data-stu-id="59c84-131">System.String</span></span>

## <span data-ttu-id="59c84-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59c84-132">OUTPUTS</span></span>

### <span data-ttu-id="59c84-133">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="59c84-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="59c84-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59c84-134">NOTES</span></span>

## <span data-ttu-id="59c84-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59c84-135">RELATED LINKS</span></span>
