---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763537"
---
# <span data-ttu-id="a421d-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a421d-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a421d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a421d-102">SYNOPSIS</span></span>
<span data-ttu-id="a421d-103">SQL veritabanının geri yüklenebildiği yeni bir geri yükleme noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a421d-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a421d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a421d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a421d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a421d-105">DESCRIPTION</span></span>
<span data-ttu-id="a421d-106">**New-AzureRmSqlDatabaseRestorePoint** cmdlet 'ı BIR Azure SQL veritabanının geri yüklenebileceğini belirten yeni bir geri yükleme noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a421d-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="a421d-107">Bu cmdlet Şu anda Azure SQL veritabanında SQL Server DataWarehouse hizmeti tarafından desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="a421d-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="a421d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a421d-108">EXAMPLES</span></span>

### <span data-ttu-id="a421d-109">Örnek 1: geri yükleme noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="a421d-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="a421d-110">Bu komut, Azure SQL veritabanı için geri yükleme noktası oluşturur ve geri yükleme noktasının ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a421d-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="a421d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a421d-111">PARAMETERS</span></span>

### <span data-ttu-id="a421d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a421d-112">-DatabaseName</span></span>
<span data-ttu-id="a421d-113">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a421d-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a421d-114">-DefaultProfile</span></span>
<span data-ttu-id="a421d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a421d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a421d-116">-ResourceGroupName</span></span>
<span data-ttu-id="a421d-117">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a421d-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="a421d-118">-RestorePointLabel</span></span>
<span data-ttu-id="a421d-119">Kolay tanımlama için geri yükleme noktasının etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a421d-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a421d-120">-ServerName</span></span>
<span data-ttu-id="a421d-121">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a421d-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a421d-122">-Confirm</span></span>
<span data-ttu-id="a421d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a421d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a421d-124">-WhatIf</span></span>
<span data-ttu-id="a421d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a421d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a421d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a421d-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a421d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a421d-127">CommonParameters</span></span>
<span data-ttu-id="a421d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a421d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a421d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a421d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a421d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a421d-130">INPUTS</span></span>

## <span data-ttu-id="a421d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a421d-131">OUTPUTS</span></span>

## <span data-ttu-id="a421d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a421d-132">NOTES</span></span>

## <span data-ttu-id="a421d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a421d-133">RELATED LINKS</span></span>
