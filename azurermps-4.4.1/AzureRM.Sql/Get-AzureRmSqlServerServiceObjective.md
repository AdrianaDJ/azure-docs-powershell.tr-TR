---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764211"
---
# <span data-ttu-id="91c51-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="91c51-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="91c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c51-102">SYNOPSIS</span></span>
<span data-ttu-id="91c51-103">Bir Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c51-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91c51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91c51-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91c51-105">DESCRIPTION</span></span>
<span data-ttu-id="91c51-106">**Get-Azurermsqlserverserviceamacın** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için kullanılabilir hizmet hedeflerini alır.</span><span class="sxs-lookup"><span data-stu-id="91c51-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="91c51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91c51-107">EXAMPLES</span></span>

### <span data-ttu-id="91c51-108">Örnek 1: hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="91c51-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="91c51-109">Bu komut, server01 adlı sunucu ve Database01 adlı veritabanı için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c51-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="91c51-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91c51-110">PARAMETERS</span></span>

### <span data-ttu-id="91c51-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91c51-111">-DatabaseName</span></span>
<span data-ttu-id="91c51-112">Azure SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c51-112">Specifies the name of an Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c51-113">-ResourceGroupName</span></span>
<span data-ttu-id="91c51-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c51-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="91c51-115">Bu cmdlet, bu kaynağa atanmış bir SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="91c51-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="91c51-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="91c51-116">-ServerName</span></span>
<span data-ttu-id="91c51-117">SQL veritabanı SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c51-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="91c51-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="91c51-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="91c51-119">Azure SQL veritabanı sunucusu için hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91c51-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="91c51-120">Bu parametre için kabul edilebilir değerler: Basic, S0, S1, S2, P1, P2 ve P3.</span><span class="sxs-lookup"><span data-stu-id="91c51-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c51-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="91c51-121">-Confirm</span></span>
<span data-ttu-id="91c51-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91c51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c51-123">-WhatIf</span></span>
<span data-ttu-id="91c51-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91c51-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c51-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91c51-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c51-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c51-126">-DefaultProfile</span></span>
<span data-ttu-id="91c51-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91c51-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c51-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c51-128">CommonParameters</span></span>
<span data-ttu-id="91c51-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91c51-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c51-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c51-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c51-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91c51-131">INPUTS</span></span>

## <span data-ttu-id="91c51-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91c51-132">OUTPUTS</span></span>

### <span data-ttu-id="91c51-133">Microsoft. Azure. Commands. Sql. Serviceamacın. model. azures, Serverserviceobjectivemodel</span><span class="sxs-lookup"><span data-stu-id="91c51-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="91c51-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91c51-134">NOTES</span></span>

## <span data-ttu-id="91c51-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91c51-135">RELATED LINKS</span></span>

[<span data-ttu-id="91c51-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="91c51-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


