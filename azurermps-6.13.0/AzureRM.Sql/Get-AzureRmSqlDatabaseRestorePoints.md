---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: c1e4c22392087793e6fbfa0e3959a8b92767ad04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763433"
---
# <span data-ttu-id="60aa5-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="60aa5-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="60aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="60aa5-103">SQL veri ambarının geri yüklenebildiği ayrı geri yükleme noktalarını getirir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60aa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60aa5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60aa5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="60aa5-106">**Get-AzureRmSqlDatabaseRestorePoints** cmdlet 'ı, Azure SQL veri ambarının geri yüklenemeyebilecek ayrı geri yükleme noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="60aa5-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="60aa5-107">Azure SQL veritabanı için, geri yükleme penceresi kesintisiz olur.</span><span class="sxs-lookup"><span data-stu-id="60aa5-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="60aa5-108">Bu, veritabanının yedekleme bekletme dönemindeki herhangi bir noktanın geri yükleme noktası olarak kullanılabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="60aa5-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="60aa5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60aa5-110">EXAMPLES</span></span>

### <span data-ttu-id="60aa5-111">Örnek 1: tüm geri yükleme noktalarını alma</span><span class="sxs-lookup"><span data-stu-id="60aa5-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="60aa5-112">Bu komut, Database01 adlı Azure SQL veritabanı için kullanılabilir tüm geri yükleme noktalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="60aa5-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="60aa5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60aa5-113">PARAMETERS</span></span>

### <span data-ttu-id="60aa5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60aa5-114">-DatabaseName</span></span>
<span data-ttu-id="60aa5-115">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="60aa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aa5-116">-DefaultProfile</span></span>
<span data-ttu-id="60aa5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="60aa5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60aa5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aa5-118">-ResourceGroupName</span></span>
<span data-ttu-id="60aa5-119">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="60aa5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60aa5-120">-ServerName</span></span>
<span data-ttu-id="60aa5-121">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="60aa5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="60aa5-122">-Confirm</span></span>
<span data-ttu-id="60aa5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60aa5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60aa5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60aa5-124">-WhatIf</span></span>
<span data-ttu-id="60aa5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60aa5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60aa5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60aa5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60aa5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aa5-127">CommonParameters</span></span>
<span data-ttu-id="60aa5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60aa5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aa5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60aa5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aa5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60aa5-130">INPUTS</span></span>

### <span data-ttu-id="60aa5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="60aa5-131">System.String</span></span>

## <span data-ttu-id="60aa5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60aa5-132">OUTPUTS</span></span>

### <span data-ttu-id="60aa5-133">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="60aa5-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="60aa5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60aa5-134">NOTES</span></span>

## <span data-ttu-id="60aa5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60aa5-135">RELATED LINKS</span></span>
