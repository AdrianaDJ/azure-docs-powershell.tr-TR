---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 597156e101a9d16eff36d05fae71b32e0033ad6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590001"
---
# <span data-ttu-id="bdc79-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="bdc79-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="bdc79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc79-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc79-103">Azure SQL veritabanı sunucusunu yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdc79-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdc79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdc79-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdc79-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc79-106">**Get-AzureRmSqlServerUpgradeHint** cmdlet 'i, BIR Azure SQL veritabanı sunucusunu yükseltmek için fiyatlandırma katmanı ipuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdc79-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="bdc79-107">İpuçları, elastik veritabanı havuzu ve tek başına veritabanı ipuçlarını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="bdc79-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="bdc79-108">Hala Web ve Iş fiyatlandırması katmanlarındaki veritabanları, yeni temel, standart veya Premium fiyatlandırma katmanlarına yükseltme veya elastik veritabanı havuzuna katılma ipucu alın.</span><span class="sxs-lookup"><span data-stu-id="bdc79-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="bdc79-109">Bu cmdlet belirtilen sunucuda barındırılan tüm veritabanlarının ipuçlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="bdc79-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="bdc79-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdc79-110">EXAMPLES</span></span>

### <span data-ttu-id="bdc79-111">Örnek 1: Birleşik önerileri alın</span><span class="sxs-lookup"><span data-stu-id="bdc79-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="bdc79-112">Bu komut, server01 adlı sunucudaki tüm veritabanları için Birleşik önerileri alır.</span><span class="sxs-lookup"><span data-stu-id="bdc79-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="bdc79-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdc79-113">PARAMETERS</span></span>

### <span data-ttu-id="bdc79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc79-114">-DefaultProfile</span></span>
<span data-ttu-id="bdc79-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bdc79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc79-116">-Excludeelavepools</span><span class="sxs-lookup"><span data-stu-id="bdc79-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="bdc79-117">Elastik veritabanı havuzlarına eklenen veritabanlarının döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdc79-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="bdc79-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc79-118">-ResourceGroupName</span></span>
<span data-ttu-id="bdc79-119">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdc79-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bdc79-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bdc79-120">-ServerName</span></span>
<span data-ttu-id="bdc79-121">Bu cmdlet 'in yükseltme ipucu aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdc79-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="bdc79-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdc79-122">-Confirm</span></span>
<span data-ttu-id="bdc79-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdc79-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc79-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc79-124">-WhatIf</span></span>
<span data-ttu-id="bdc79-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdc79-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc79-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdc79-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc79-127">CommonParameters</span></span>
<span data-ttu-id="bdc79-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdc79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc79-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc79-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdc79-130">INPUTS</span></span>

### <span data-ttu-id="bdc79-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc79-131">System.String</span></span>

### <span data-ttu-id="bdc79-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdc79-132">System.Boolean</span></span>

## <span data-ttu-id="bdc79-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdc79-133">OUTPUTS</span></span>

### <span data-ttu-id="bdc79-134">Microsoft. Azure. Commands. Sql. ServiceTierAdvisor. model. Upgradeserveripucu</span><span class="sxs-lookup"><span data-stu-id="bdc79-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="bdc79-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdc79-135">NOTES</span></span>

## <span data-ttu-id="bdc79-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdc79-136">RELATED LINKS</span></span>

[<span data-ttu-id="bdc79-137">Get-Azurermsqldatabasegenişletilen</span><span class="sxs-lookup"><span data-stu-id="bdc79-137">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="bdc79-138">Get-Azurermsqlelakpoolönerisi</span><span class="sxs-lookup"><span data-stu-id="bdc79-138">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="bdc79-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="bdc79-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


