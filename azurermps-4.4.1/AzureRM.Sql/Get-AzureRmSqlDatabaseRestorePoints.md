---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: 002b248195840cb7453757e92f9269e7a61d9fda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591764"
---
# <span data-ttu-id="dc3bb-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="dc3bb-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="dc3bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3bb-103">SQL veri ambarının geri yüklenebildiği ayrı geri yükleme noktalarını getirir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc3bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc3bb-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc3bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc3bb-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3bb-106">**Get-AzureRmSqlDatabaseRestorePoints** cmdlet 'ı, Azure SQL veri ambarının geri yüklenemeyebilecek ayrı geri yükleme noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="dc3bb-107">Azure SQL veritabanı için, geri yükleme penceresi kesintisiz olur.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="dc3bb-108">Bu, veritabanının yedekleme bekletme dönemindeki herhangi bir noktanın geri yükleme noktası olarak kullanılabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="dc3bb-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="dc3bb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc3bb-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3bb-111">Örnek 1: tüm geri yükleme noktalarını alma</span><span class="sxs-lookup"><span data-stu-id="dc3bb-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
```

<span data-ttu-id="dc3bb-112">Bu komut, Database01 adlı Azure SQL veritabanı için kullanılabilir tüm geri yükleme noktalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="dc3bb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc3bb-113">PARAMETERS</span></span>

### <span data-ttu-id="dc3bb-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc3bb-114">-DatabaseName</span></span>
<span data-ttu-id="dc3bb-115">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="dc3bb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc3bb-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc3bb-117">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="dc3bb-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc3bb-118">-ServerName</span></span>
<span data-ttu-id="dc3bb-119">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-119">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="dc3bb-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc3bb-120">-Confirm</span></span>
<span data-ttu-id="dc3bb-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3bb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3bb-122">-WhatIf</span></span>
<span data-ttu-id="dc3bb-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3bb-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3bb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3bb-125">-DefaultProfile</span></span>
<span data-ttu-id="dc3bb-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3bb-127">CommonParameters</span></span>
<span data-ttu-id="dc3bb-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc3bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3bb-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3bb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3bb-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc3bb-130">INPUTS</span></span>

## <span data-ttu-id="dc3bb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc3bb-131">OUTPUTS</span></span>

## <span data-ttu-id="dc3bb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc3bb-132">NOTES</span></span>

## <span data-ttu-id="dc3bb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc3bb-133">RELATED LINKS</span></span>
