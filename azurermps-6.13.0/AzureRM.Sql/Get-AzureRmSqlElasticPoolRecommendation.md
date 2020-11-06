---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 0769824bc0b50641f7b73cb530dde0a5f30bf7ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590011"
---
# <span data-ttu-id="9296f-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="9296f-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="9296f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9296f-102">SYNOPSIS</span></span>
<span data-ttu-id="9296f-103">Elastik havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9296f-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9296f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9296f-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9296f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9296f-105">DESCRIPTION</span></span>
<span data-ttu-id="9296f-106">**Get-Azurermsqlelaraz Pooltavsiye** cmdlet 'i bir sunucu için elastik havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9296f-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="9296f-107">Bu öneriler aşağıdaki değerleri içerir:</span><span class="sxs-lookup"><span data-stu-id="9296f-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="9296f-108">Veritabanı koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="9296f-108">DatabaseCollection.</span></span> <span data-ttu-id="9296f-109">Havuza ait veritabanı adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="9296f-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="9296f-110">Databasedtumın.</span><span class="sxs-lookup"><span data-stu-id="9296f-110">DatabaseDtuMin.</span></span> <span data-ttu-id="9296f-111">Elastik havuzda veri aktarım birimi (DTU) garantisi.</span><span class="sxs-lookup"><span data-stu-id="9296f-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="9296f-112">--Databasevseçtumax.</span><span class="sxs-lookup"><span data-stu-id="9296f-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="9296f-113">Elastik havuzdaki veritabanları için DTU Cap.</span><span class="sxs-lookup"><span data-stu-id="9296f-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="9296f-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="9296f-114">Dtu.</span></span> <span data-ttu-id="9296f-115">Esnek havuzun DTU garantisi.</span><span class="sxs-lookup"><span data-stu-id="9296f-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="9296f-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="9296f-116">StorageMb.</span></span> <span data-ttu-id="9296f-117">Esnek havuz için megabayt cinsinden depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="9296f-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="9296f-118">EDI.</span><span class="sxs-lookup"><span data-stu-id="9296f-118">Edition.</span></span> <span data-ttu-id="9296f-119">.</span><span class="sxs-lookup"><span data-stu-id="9296f-119">Edition for the elastic pool.</span></span> <span data-ttu-id="9296f-120">Bu parametre için kabul edilebilir değerler: temel, standart ve Premium.</span><span class="sxs-lookup"><span data-stu-id="9296f-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="9296f-121">Includealldatabases.</span><span class="sxs-lookup"><span data-stu-id="9296f-121">IncludeAllDatabases.</span></span> <span data-ttu-id="9296f-122">Elastik havuzdaki tüm veritabanlarının gönderilip gönderilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9296f-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="9296f-123">Adlandır.</span><span class="sxs-lookup"><span data-stu-id="9296f-123">Name.</span></span> <span data-ttu-id="9296f-124">Esnek havuzun adı.</span><span class="sxs-lookup"><span data-stu-id="9296f-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="9296f-125">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9296f-125">EXAMPLES</span></span>

### <span data-ttu-id="9296f-126">Örnek 1: sunucunun önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="9296f-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="9296f-127">Bu komut, server01 adlı sunucu için esnek havuz önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9296f-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="9296f-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9296f-128">PARAMETERS</span></span>

### <span data-ttu-id="9296f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9296f-129">-DefaultProfile</span></span>
<span data-ttu-id="9296f-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9296f-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9296f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9296f-131">-ResourceGroupName</span></span>
<span data-ttu-id="9296f-132">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9296f-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9296f-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9296f-133">-ServerName</span></span>
<span data-ttu-id="9296f-134">Bu cmdlet 'in öneri aldığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9296f-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="9296f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="9296f-135">-Confirm</span></span>
<span data-ttu-id="9296f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9296f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9296f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9296f-137">-WhatIf</span></span>
<span data-ttu-id="9296f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9296f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9296f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9296f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9296f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9296f-140">CommonParameters</span></span>
<span data-ttu-id="9296f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9296f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9296f-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9296f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9296f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9296f-143">INPUTS</span></span>

### <span data-ttu-id="9296f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9296f-144">System.String</span></span>

## <span data-ttu-id="9296f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9296f-145">OUTPUTS</span></span>

### <span data-ttu-id="9296f-146">Microsoft. Azure. Management. Sql. LegacySdk. modeller. Yükseldereyorumdedelaçıkartpoolproperties</span><span class="sxs-lookup"><span data-stu-id="9296f-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="9296f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9296f-147">NOTES</span></span>

## <span data-ttu-id="9296f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9296f-148">RELATED LINKS</span></span>
