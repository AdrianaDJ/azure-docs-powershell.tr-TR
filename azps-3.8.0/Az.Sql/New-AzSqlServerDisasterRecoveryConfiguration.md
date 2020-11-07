---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938418"
---
# <span data-ttu-id="1f0ae-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f0ae-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="1f0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0ae-103">Veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="1f0ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f0ae-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f0ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="1f0ae-106">**New-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="1f0ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f0ae-107">EXAMPLES</span></span>

## <span data-ttu-id="1f0ae-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f0ae-108">PARAMETERS</span></span>

### <span data-ttu-id="1f0ae-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f0ae-109">-AsJob</span></span>
<span data-ttu-id="1f0ae-110">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1f0ae-110">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0ae-111">-DefaultProfile</span></span>
<span data-ttu-id="1f0ae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1f0ae-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f0ae-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1f0ae-113">-FailoverPolicy</span></span>
<span data-ttu-id="1f0ae-114">Yerine çalışma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0ae-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0ae-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1f0ae-116">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0ae-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1f0ae-117">-PartnerServerName</span></span>
<span data-ttu-id="1f0ae-118">İş ortağı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-118">Specifies the name of the partner server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f0ae-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1f0ae-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f0ae-121">-ServerName</span></span>
<span data-ttu-id="1f0ae-122">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1f0ae-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="1f0ae-123">-VirtualEndpointName</span></span>
<span data-ttu-id="1f0ae-124">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0ae-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f0ae-125">-Confirm</span></span>
<span data-ttu-id="1f0ae-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f0ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f0ae-127">-WhatIf</span></span>
<span data-ttu-id="1f0ae-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f0ae-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f0ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0ae-130">CommonParameters</span></span>
<span data-ttu-id="1f0ae-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0ae-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f0ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0ae-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f0ae-133">INPUTS</span></span>

### <span data-ttu-id="1f0ae-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f0ae-134">System.String</span></span>

## <span data-ttu-id="1f0ae-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f0ae-135">OUTPUTS</span></span>

### <span data-ttu-id="1f0ae-136">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="1f0ae-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="1f0ae-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f0ae-137">NOTES</span></span>

## <span data-ttu-id="1f0ae-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f0ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f0ae-139">Get-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="1f0ae-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1f0ae-140">Remove-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="1f0ae-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1f0ae-141">Set-Azsqlserverdederecoveryconfiguration</span><span class="sxs-lookup"><span data-stu-id="1f0ae-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1f0ae-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1f0ae-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
