---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 13ce7a2410f8231d4c5194fbd57d41074d0ca892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587153"
---
# <span data-ttu-id="42dda-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="42dda-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="42dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dda-102">SYNOPSIS</span></span>
<span data-ttu-id="42dda-103">Bir Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42dda-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42dda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42dda-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42dda-105">DESCRIPTION</span></span>
<span data-ttu-id="42dda-106">**Get-Azurermsqlserverserviceamacın** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için kullanılabilir hizmet hedeflerini alır.</span><span class="sxs-lookup"><span data-stu-id="42dda-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="42dda-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42dda-107">EXAMPLES</span></span>

### <span data-ttu-id="42dda-108">Örnek 1: hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="42dda-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="42dda-109">Bu komut, server01 adlı sunucu ve Database01 adlı veritabanı için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42dda-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="42dda-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42dda-110">PARAMETERS</span></span>

### <span data-ttu-id="42dda-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42dda-111">-DatabaseName</span></span>
<span data-ttu-id="42dda-112">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="42dda-112">SQL Database name.</span></span>

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

### <span data-ttu-id="42dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dda-113">-DefaultProfile</span></span>
<span data-ttu-id="42dda-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42dda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42dda-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dda-115">-ResourceGroupName</span></span>
<span data-ttu-id="42dda-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42dda-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="42dda-117">Bu cmdlet, bu kaynağa atanmış bir SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42dda-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="42dda-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42dda-118">-ServerName</span></span>
<span data-ttu-id="42dda-119">SQL veritabanı SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42dda-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="42dda-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="42dda-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="42dda-121">Azure SQL veritabanı sunucusu için hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42dda-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="42dda-122">Bu parametre için kabul edilebilir değerler: Basic, S0, S1, S2, P1, P2 ve P3.</span><span class="sxs-lookup"><span data-stu-id="42dda-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="42dda-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="42dda-123">-Confirm</span></span>
<span data-ttu-id="42dda-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42dda-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dda-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dda-125">-WhatIf</span></span>
<span data-ttu-id="42dda-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42dda-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dda-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42dda-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dda-128">CommonParameters</span></span>
<span data-ttu-id="42dda-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42dda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dda-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dda-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dda-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42dda-131">INPUTS</span></span>

### <span data-ttu-id="42dda-132">System. String</span><span class="sxs-lookup"><span data-stu-id="42dda-132">System.String</span></span>

## <span data-ttu-id="42dda-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42dda-133">OUTPUTS</span></span>

### <span data-ttu-id="42dda-134">Microsoft. Azure. Commands. Sql. Serviceamacın. model. azures, Serverserviceobjectivemodel</span><span class="sxs-lookup"><span data-stu-id="42dda-134">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="42dda-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42dda-135">NOTES</span></span>

## <span data-ttu-id="42dda-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42dda-136">RELATED LINKS</span></span>

[<span data-ttu-id="42dda-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="42dda-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


