---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 18dcc69746e46ba75c01cb3aeb935bdd6b25d3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587765"
---
# <span data-ttu-id="0b006-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="0b006-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="0b006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b006-102">SYNOPSIS</span></span>
<span data-ttu-id="0b006-103">Azure SQL veritabanı sunucusunu yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b006-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b006-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b006-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b006-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b006-105">DESCRIPTION</span></span>
<span data-ttu-id="0b006-106">**Get-AzureRmSqlServerUpgradeHint** cmdlet 'i, BIR Azure SQL veritabanı sunucusunu yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b006-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="0b006-107">İpuçları, elastik veritabanı havuzu ve tek başına veritabanı ipuçlarını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0b006-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="0b006-108">Hala Web ve Iş fiyatlandırması katmanlarındaki veritabanları, yeni temel, standart veya Premium fiyatlandırma katmanlarına yükseltme veya elastik veritabanı havuzuna katılma ipucu alın.</span><span class="sxs-lookup"><span data-stu-id="0b006-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="0b006-109">Bu cmdlet belirtilen sunucuda barındırılan tüm veritabanlarının ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b006-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="0b006-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b006-110">EXAMPLES</span></span>

### <span data-ttu-id="0b006-111">Örnek 1: Birleşik önerileri alın</span><span class="sxs-lookup"><span data-stu-id="0b006-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="0b006-112">Bu komut, server01 adlı sunucudaki tüm veritabanları için Birleşik önerileri alır.</span><span class="sxs-lookup"><span data-stu-id="0b006-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="0b006-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b006-113">PARAMETERS</span></span>

### <span data-ttu-id="0b006-114">-Excludeelavepools</span><span class="sxs-lookup"><span data-stu-id="0b006-114">-ExcludeElasticPools</span></span>
<span data-ttu-id="0b006-115">Elastik veritabanı havuzlarına eklenen veritabanlarının döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b006-115">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b006-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b006-116">-ResourceGroupName</span></span>
<span data-ttu-id="0b006-117">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b006-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0b006-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b006-118">-ServerName</span></span>
<span data-ttu-id="0b006-119">Bu cmdlet 'in yükseltme ipucu aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b006-119">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="0b006-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b006-120">-Confirm</span></span>
<span data-ttu-id="0b006-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b006-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b006-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b006-122">-WhatIf</span></span>
<span data-ttu-id="0b006-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b006-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b006-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b006-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b006-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b006-125">-DefaultProfile</span></span>
<span data-ttu-id="0b006-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b006-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b006-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b006-127">CommonParameters</span></span>
<span data-ttu-id="0b006-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b006-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b006-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b006-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b006-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b006-130">INPUTS</span></span>

## <span data-ttu-id="0b006-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b006-131">OUTPUTS</span></span>

## <span data-ttu-id="0b006-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b006-132">NOTES</span></span>

## <span data-ttu-id="0b006-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b006-133">RELATED LINKS</span></span>

[<span data-ttu-id="0b006-134">Get-Azurermsqldatabasegenişletilen</span><span class="sxs-lookup"><span data-stu-id="0b006-134">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="0b006-135">Get-Azurermsqlelakpoolönerisi</span><span class="sxs-lookup"><span data-stu-id="0b006-135">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="0b006-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0b006-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


