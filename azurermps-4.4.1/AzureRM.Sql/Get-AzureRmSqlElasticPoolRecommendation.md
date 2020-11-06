---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589040"
---
# <span data-ttu-id="edab1-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="edab1-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="edab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edab1-102">SYNOPSIS</span></span>
<span data-ttu-id="edab1-103">Elastik havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="edab1-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edab1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edab1-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edab1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edab1-105">DESCRIPTION</span></span>
<span data-ttu-id="edab1-106">**Get-Azurermsqlelaraz Pooltavsiye** cmdlet 'i bir sunucu için elastik havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="edab1-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="edab1-107">Bu öneriler aşağıdaki değerleri içerir:</span><span class="sxs-lookup"><span data-stu-id="edab1-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="edab1-108">Veritabanı koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="edab1-108">DatabaseCollection.</span></span> <span data-ttu-id="edab1-109">Havuza ait veritabanı adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="edab1-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="edab1-110">Databasedtumın.</span><span class="sxs-lookup"><span data-stu-id="edab1-110">DatabaseDtuMin.</span></span> <span data-ttu-id="edab1-111">Elastik havuzda veri aktarım birimi (DTU) garantisi.</span><span class="sxs-lookup"><span data-stu-id="edab1-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="edab1-112">--Databasevseçtumax.</span><span class="sxs-lookup"><span data-stu-id="edab1-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="edab1-113">Elastik havuzdaki veritabanları için DTU Cap.</span><span class="sxs-lookup"><span data-stu-id="edab1-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="edab1-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="edab1-114">Dtu.</span></span> <span data-ttu-id="edab1-115">Esnek havuzun DTU garantisi.</span><span class="sxs-lookup"><span data-stu-id="edab1-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="edab1-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="edab1-116">StorageMb.</span></span> <span data-ttu-id="edab1-117">Esnek havuz için megabayt cinsinden depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="edab1-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="edab1-118">EDI.</span><span class="sxs-lookup"><span data-stu-id="edab1-118">Edition.</span></span> <span data-ttu-id="edab1-119">.</span><span class="sxs-lookup"><span data-stu-id="edab1-119">Edition for the elastic pool.</span></span> <span data-ttu-id="edab1-120">Bu parametre için kabul edilebilir değerler: temel, standart ve Premium.</span><span class="sxs-lookup"><span data-stu-id="edab1-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="edab1-121">Includealldatabases.</span><span class="sxs-lookup"><span data-stu-id="edab1-121">IncludeAllDatabases.</span></span> <span data-ttu-id="edab1-122">Elastik havuzdaki tüm veritabanlarının gönderilip gönderilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="edab1-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="edab1-123">Adlandır.</span><span class="sxs-lookup"><span data-stu-id="edab1-123">Name.</span></span> <span data-ttu-id="edab1-124">Esnek havuzun adı.</span><span class="sxs-lookup"><span data-stu-id="edab1-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="edab1-125">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edab1-125">EXAMPLES</span></span>

### <span data-ttu-id="edab1-126">Örnek 1: sunucunun önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="edab1-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="edab1-127">Bu komut, server01 adlı sunucu için esnek havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="edab1-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="edab1-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edab1-128">PARAMETERS</span></span>

### <span data-ttu-id="edab1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edab1-129">-ResourceGroupName</span></span>
<span data-ttu-id="edab1-130">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edab1-130">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="edab1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edab1-131">-ServerName</span></span>
<span data-ttu-id="edab1-132">Bu cmdlet 'in öneri aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edab1-132">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="edab1-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="edab1-133">-Confirm</span></span>
<span data-ttu-id="edab1-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edab1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edab1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edab1-135">-WhatIf</span></span>
<span data-ttu-id="edab1-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edab1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edab1-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edab1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edab1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edab1-138">-DefaultProfile</span></span>
<span data-ttu-id="edab1-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edab1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edab1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edab1-140">CommonParameters</span></span>
<span data-ttu-id="edab1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edab1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edab1-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edab1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edab1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edab1-143">INPUTS</span></span>

## <span data-ttu-id="edab1-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edab1-144">OUTPUTS</span></span>

## <span data-ttu-id="edab1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edab1-145">NOTES</span></span>

## <span data-ttu-id="edab1-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edab1-146">RELATED LINKS</span></span>

