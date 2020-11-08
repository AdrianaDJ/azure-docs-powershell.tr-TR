---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096258"
---
# <span data-ttu-id="e2989-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="e2989-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="e2989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2989-102">SYNOPSIS</span></span>
<span data-ttu-id="e2989-103">Bir Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e2989-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2989-104">SYNTAX</span></span>

### <span data-ttu-id="e2989-105">ByLocation (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2989-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2989-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="e2989-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2989-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2989-107">DESCRIPTION</span></span>
<span data-ttu-id="e2989-108">**Get-Azsqlserverserviceamacın** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için kullanılabilir hizmet hedeflerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e2989-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2989-109">EXAMPLES</span></span>

### <span data-ttu-id="e2989-110">Örnek 1: hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="e2989-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="e2989-111">Bu komut, server01 adlı sunucunun hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="e2989-112">Örnek 2: filtreleme kullanarak hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="e2989-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="e2989-113">Bu komut, "System" ile başlayan server01 adındaki sunucunun hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="e2989-114">Örnek 3: bir konum için hizmet amaçlarını alma</span><span class="sxs-lookup"><span data-stu-id="e2989-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="e2989-115">Bu komut belirtilen bir Azure bölgesinin hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="e2989-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2989-116">PARAMETERS</span></span>

### <span data-ttu-id="e2989-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2989-117">-DefaultProfile</span></span>
<span data-ttu-id="e2989-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2989-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2989-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e2989-119">-Location</span></span>
<span data-ttu-id="e2989-120">Hizmet hedeflerine alınacak konumun adı.</span><span class="sxs-lookup"><span data-stu-id="e2989-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2989-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2989-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2989-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2989-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e2989-123">Bu cmdlet, bu kaynağa atanmış bir SQL veritabanı sunucusu için hizmet amaçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e2989-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2989-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2989-124">-ServerName</span></span>
<span data-ttu-id="e2989-125">SQL veritabanı SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2989-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2989-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e2989-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="e2989-127">Azure SQL veritabanı sunucusu için hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2989-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="e2989-128">Bu parametre için kabul edilebilir değerler: Basic, S0, S1, S2, P1, P2 ve P3.</span><span class="sxs-lookup"><span data-stu-id="e2989-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="e2989-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2989-129">-Confirm</span></span>
<span data-ttu-id="e2989-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2989-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2989-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2989-131">-WhatIf</span></span>
<span data-ttu-id="e2989-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2989-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2989-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2989-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2989-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2989-134">CommonParameters</span></span>
<span data-ttu-id="e2989-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2989-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2989-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2989-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2989-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2989-137">INPUTS</span></span>

### <span data-ttu-id="e2989-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2989-138">System.String</span></span>

## <span data-ttu-id="e2989-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2989-139">OUTPUTS</span></span>

### <span data-ttu-id="e2989-140">Microsoft. Azure. Commands. Sql. Serviceamacın. model. azures, Serverserviceobjectivemodel</span><span class="sxs-lookup"><span data-stu-id="e2989-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="e2989-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2989-141">NOTES</span></span>

## <span data-ttu-id="e2989-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2989-142">RELATED LINKS</span></span>

[<span data-ttu-id="e2989-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e2989-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


