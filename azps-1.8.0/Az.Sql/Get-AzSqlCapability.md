---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: b729f1cfdb0dd030456e1dffc85c82171a315cb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759056"
---
# <span data-ttu-id="b841a-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b841a-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="b841a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b841a-102">SYNOPSIS</span></span>
<span data-ttu-id="b841a-103">Geçerli aboneliğin SQL veritabanı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b841a-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="b841a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b841a-104">SYNTAX</span></span>

### <span data-ttu-id="b841a-105">FilterResults (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b841a-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b841a-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="b841a-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b841a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b841a-107">DESCRIPTION</span></span>
<span data-ttu-id="b841a-108">**Get-AzSqlCapability** cmdlet 'i, bir bölge için geçerli abonelikte sağlanan Azure SQL veritabanı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b841a-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="b841a-109">*Serverversionname* , *SürümAdı* veya *serviceobjectivename* parametrelerini belirtirseniz, bu cmdlet belirtilen değerleri ve bunların öncüllerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b841a-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="b841a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b841a-110">EXAMPLES</span></span>

### <span data-ttu-id="b841a-111">Örnek 1: bir bölgeye yönelik geçerli aboneliğin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="b841a-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="b841a-112">Bu komut, Merkezi ABD bölgesi için geçerli abonelikteki SQL veritabanı örneklerinin özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b841a-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="b841a-113">Örnek 2: bir bölgeye yönelik geçerli aboneliğin varsayılan özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="b841a-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="b841a-114">Bu komut, Merkezi ABD bölgesindeki geçerli abonelikteki SQL veritabanları için varsayılan özellikleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="b841a-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="b841a-115">Örnek 3: hizmet hedefi için ayrıntıları alma</span><span class="sxs-lookup"><span data-stu-id="b841a-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="b841a-116">Bu komut, geçerli abonelikteki belirtilen hizmet hedefi için SQL veritabanları için varsayılan özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b841a-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="b841a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b841a-117">PARAMETERS</span></span>

### <span data-ttu-id="b841a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b841a-118">-DefaultProfile</span></span>
<span data-ttu-id="b841a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b841a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b841a-120">-Varsayılanlar</span><span class="sxs-lookup"><span data-stu-id="b841a-120">-Defaults</span></span>
<span data-ttu-id="b841a-121">Bu cmdlet 'in yalnızca Varsayılanları aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b841a-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b841a-122">-SürümAdı</span><span class="sxs-lookup"><span data-stu-id="b841a-122">-EditionName</span></span>
<span data-ttu-id="b841a-123">Bu cmdlet 'in yetenek aldığı veritabanı sürümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b841a-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b841a-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="b841a-124">-LocationName</span></span>
<span data-ttu-id="b841a-125">Bu cmdlet 'in yetenek aldığı konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b841a-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="b841a-126">Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/regions/ https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="b841a-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="b841a-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="b841a-127">-ServerVersionName</span></span>
<span data-ttu-id="b841a-128">Bu cmdlet 'in özellikleri aldığı sunucu sürümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b841a-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b841a-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b841a-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="b841a-130">Bu cmdlet 'in yetenekleri aldığı hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b841a-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b841a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="b841a-131">-Confirm</span></span>
<span data-ttu-id="b841a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b841a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b841a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b841a-133">-WhatIf</span></span>
<span data-ttu-id="b841a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b841a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b841a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b841a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b841a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b841a-136">CommonParameters</span></span>
<span data-ttu-id="b841a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b841a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b841a-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b841a-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b841a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b841a-139">INPUTS</span></span>

### <span data-ttu-id="b841a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b841a-140">System.String</span></span>

## <span data-ttu-id="b841a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b841a-141">OUTPUTS</span></span>

### <span data-ttu-id="b841a-142">Microsoft.Azure.Commands.Sql.Location_Capabilities. model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="b841a-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="b841a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b841a-143">NOTES</span></span>

## <span data-ttu-id="b841a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b841a-144">RELATED LINKS</span></span>
