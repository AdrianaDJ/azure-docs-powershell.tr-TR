---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: f574e8e67f249ac1c7a4a3878ecc93a0a1eabc5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588702"
---
# <span data-ttu-id="1304c-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1304c-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="1304c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1304c-102">SYNOPSIS</span></span>
<span data-ttu-id="1304c-103">Bir veritabanı coğrafi yedekleme ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1304c-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1304c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1304c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1304c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1304c-105">DESCRIPTION</span></span>
<span data-ttu-id="1304c-106">**Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet 'i veritabanına kaydedilen coğrafi yedekleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1304c-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="1304c-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1304c-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="1304c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1304c-108">EXAMPLES</span></span>

## <span data-ttu-id="1304c-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1304c-109">PARAMETERS</span></span>

### <span data-ttu-id="1304c-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1304c-110">-DatabaseName</span></span>
<span data-ttu-id="1304c-111">Bu cmdlet 'in coğrafi yedekleme ilkesini ayarladığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1304c-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="1304c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1304c-112">-DefaultProfile</span></span>
<span data-ttu-id="1304c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1304c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1304c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1304c-114">-ResourceGroupName</span></span>
<span data-ttu-id="1304c-115">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1304c-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1304c-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1304c-116">-ServerName</span></span>
<span data-ttu-id="1304c-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1304c-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1304c-118">Durumlu</span><span class="sxs-lookup"><span data-stu-id="1304c-118">-State</span></span>
<span data-ttu-id="1304c-119">Coğrafi yedekleme ilkesinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1304c-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="1304c-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1304c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1304c-121">Etkin</span><span class="sxs-lookup"><span data-stu-id="1304c-121">Enabled</span></span> 
- <span data-ttu-id="1304c-122">DISABLED</span><span class="sxs-lookup"><span data-stu-id="1304c-122">Disabled</span></span>

```yaml
Type: GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1304c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1304c-123">-Confirm</span></span>
<span data-ttu-id="1304c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1304c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1304c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1304c-125">-WhatIf</span></span>
<span data-ttu-id="1304c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1304c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1304c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1304c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1304c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1304c-128">CommonParameters</span></span>
<span data-ttu-id="1304c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1304c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1304c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1304c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1304c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1304c-131">INPUTS</span></span>

### <span data-ttu-id="1304c-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1304c-132">None</span></span>
<span data-ttu-id="1304c-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1304c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1304c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1304c-134">OUTPUTS</span></span>

## <span data-ttu-id="1304c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1304c-135">NOTES</span></span>

## <span data-ttu-id="1304c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1304c-136">RELATED LINKS</span></span>

[<span data-ttu-id="1304c-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1304c-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="1304c-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1304c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

