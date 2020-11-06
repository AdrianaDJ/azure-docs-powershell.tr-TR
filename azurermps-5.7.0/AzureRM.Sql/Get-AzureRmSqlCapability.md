---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 7d62a005455394dd1b00309adcf47bc639551a4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589665"
---
# <span data-ttu-id="5d606-101">Get-AzureRmSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5d606-101">Get-AzureRmSqlCapability</span></span>

## <span data-ttu-id="5d606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d606-102">SYNOPSIS</span></span>
<span data-ttu-id="5d606-103">Geçerli aboneliğin SQL veritabanı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d606-103">Gets SQL Database capabilities for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d606-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d606-104">SYNTAX</span></span>

### <span data-ttu-id="5d606-105">FilterResults (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d606-105">FilterResults (Default)</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d606-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="5d606-106">DefaultResults</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d606-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d606-107">DESCRIPTION</span></span>
<span data-ttu-id="5d606-108">**Get-AzureRmSqlCapability** cmdlet 'i, bir bölge için geçerli abonelikte sağlanan Azure SQL veritabanı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5d606-108">The **Get-AzureRmSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="5d606-109">*Serverversionname* , *SürümAdı* veya *serviceobjectivename* parametrelerini belirtirseniz, bu cmdlet belirtilen değerleri ve bunların öncüllerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d606-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="5d606-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d606-110">EXAMPLES</span></span>

### <span data-ttu-id="5d606-111">Örnek 1: bir bölgeye yönelik geçerli aboneliğin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5d606-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="5d606-112">Bu komut, Merkezi ABD bölgesi için geçerli abonelikteki SQL veritabanı örneklerinin özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d606-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="5d606-113">Örnek 2: bir bölgeye yönelik geçerli aboneliğin varsayılan özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5d606-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="5d606-114">Bu komut, Merkezi ABD bölgesindeki geçerli abonelikteki SQL veritabanları için varsayılan özellikleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d606-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="5d606-115">Örnek 3: hizmet hedefi için ayrıntıları alma</span><span class="sxs-lookup"><span data-stu-id="5d606-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="5d606-116">Bu komut, geçerli abonelikteki belirtilen hizmet hedefi için SQL veritabanları için varsayılan özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="5d606-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="5d606-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d606-117">PARAMETERS</span></span>

### <span data-ttu-id="5d606-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d606-118">-DefaultProfile</span></span>
<span data-ttu-id="5d606-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5d606-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d606-120">-Varsayılanlar</span><span class="sxs-lookup"><span data-stu-id="5d606-120">-Defaults</span></span>
<span data-ttu-id="5d606-121">Bu cmdlet 'in yalnızca Varsayılanları aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d606-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d606-122">-SürümAdı</span><span class="sxs-lookup"><span data-stu-id="5d606-122">-EditionName</span></span>
<span data-ttu-id="5d606-123">Bu cmdlet 'in yetenek aldığı veritabanı sürümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d606-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d606-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="5d606-124">-LocationName</span></span>
<span data-ttu-id="5d606-125">Bu cmdlet 'in yetenek aldığı konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d606-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="5d606-126">Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/regions/ https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="5d606-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="5d606-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="5d606-127">-ServerVersionName</span></span>
<span data-ttu-id="5d606-128">Bu cmdlet 'in özellikleri aldığı sunucu sürümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d606-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d606-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5d606-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="5d606-130">Bu cmdlet 'in yetenekleri aldığı hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d606-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d606-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d606-131">-Confirm</span></span>
<span data-ttu-id="5d606-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d606-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d606-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d606-133">-WhatIf</span></span>
<span data-ttu-id="5d606-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d606-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d606-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d606-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d606-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d606-136">CommonParameters</span></span>
<span data-ttu-id="5d606-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d606-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d606-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d606-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d606-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d606-139">INPUTS</span></span>

### <span data-ttu-id="5d606-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5d606-140">None</span></span>
<span data-ttu-id="5d606-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5d606-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d606-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d606-142">OUTPUTS</span></span>

### <span data-ttu-id="5d606-143">Microsoft.Azure.Commands.Sql.Location_Capabilities. model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="5d606-143">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="5d606-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d606-144">NOTES</span></span>

## <span data-ttu-id="5d606-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d606-145">RELATED LINKS</span></span>
