---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592872"
---
# <span data-ttu-id="198ee-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="198ee-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="198ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="198ee-102">SYNOPSIS</span></span>
<span data-ttu-id="198ee-103">Bir SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="198ee-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="198ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="198ee-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="198ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="198ee-105">DESCRIPTION</span></span>
<span data-ttu-id="198ee-106">**Remove-AzureRmSqlDatabaseRestorePoint** cmdlet 'ı Azure SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="198ee-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="198ee-107">Bu cmdlet Şu anda Azure SQL veritabanında SQL Server DataWarehouse hizmeti tarafından desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="198ee-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="198ee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="198ee-108">EXAMPLES</span></span>

### <span data-ttu-id="198ee-109">Örnek 1: geri yükleme noktasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="198ee-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="198ee-110">Bu komut, Azure SQL veritabanı 'nın oluşturma tarihi için geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="198ee-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="198ee-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="198ee-111">PARAMETERS</span></span>

### <span data-ttu-id="198ee-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="198ee-112">-DatabaseName</span></span>
<span data-ttu-id="198ee-113">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="198ee-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="198ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198ee-114">-DefaultProfile</span></span>
<span data-ttu-id="198ee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="198ee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="198ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="198ee-117">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="198ee-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="198ee-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="198ee-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="198ee-119">Geri yükleme noktası oluşturma tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="198ee-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198ee-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="198ee-120">-ServerName</span></span>
<span data-ttu-id="198ee-121">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="198ee-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="198ee-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="198ee-122">-Confirm</span></span>
<span data-ttu-id="198ee-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="198ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="198ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198ee-124">-WhatIf</span></span>
<span data-ttu-id="198ee-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="198ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198ee-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="198ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="198ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198ee-127">CommonParameters</span></span>
<span data-ttu-id="198ee-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="198ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198ee-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="198ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198ee-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="198ee-130">INPUTS</span></span>

## <span data-ttu-id="198ee-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="198ee-131">OUTPUTS</span></span>

## <span data-ttu-id="198ee-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="198ee-132">NOTES</span></span>

## <span data-ttu-id="198ee-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="198ee-133">RELATED LINKS</span></span>