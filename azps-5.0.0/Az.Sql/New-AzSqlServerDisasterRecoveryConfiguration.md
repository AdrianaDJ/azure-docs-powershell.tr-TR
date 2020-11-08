---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276662"
---
# <span data-ttu-id="9506a-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9506a-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="9506a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9506a-102">SYNOPSIS</span></span>
<span data-ttu-id="9506a-103">Veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9506a-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="9506a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9506a-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9506a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9506a-105">DESCRIPTION</span></span>
<span data-ttu-id="9506a-106">**New-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9506a-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="9506a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9506a-107">EXAMPLES</span></span>

## <span data-ttu-id="9506a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9506a-108">PARAMETERS</span></span>

### <span data-ttu-id="9506a-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="9506a-109">-AsJob</span></span>
<span data-ttu-id="9506a-110">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9506a-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9506a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9506a-111">-DefaultProfile</span></span>
<span data-ttu-id="9506a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9506a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9506a-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9506a-113">-FailoverPolicy</span></span>
<span data-ttu-id="9506a-114">Yerine çalışma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="9506a-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9506a-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="9506a-116">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="9506a-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="9506a-117">-PartnerServerName</span></span>
<span data-ttu-id="9506a-118">İş ortağı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="9506a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9506a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9506a-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9506a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9506a-121">-ServerName</span></span>
<span data-ttu-id="9506a-122">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9506a-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="9506a-123">-VirtualEndpointName</span></span>
<span data-ttu-id="9506a-124">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9506a-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="9506a-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="9506a-125">-Confirm</span></span>
<span data-ttu-id="9506a-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9506a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9506a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9506a-127">-WhatIf</span></span>
<span data-ttu-id="9506a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9506a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9506a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9506a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9506a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9506a-130">CommonParameters</span></span>
<span data-ttu-id="9506a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9506a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9506a-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9506a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9506a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9506a-133">INPUTS</span></span>

### <span data-ttu-id="9506a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9506a-134">System.String</span></span>

## <span data-ttu-id="9506a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9506a-135">OUTPUTS</span></span>

### <span data-ttu-id="9506a-136">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="9506a-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="9506a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9506a-137">NOTES</span></span>

## <span data-ttu-id="9506a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9506a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9506a-139">Get-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9506a-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9506a-140">Remove-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9506a-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9506a-141">Set-Azsqlserverdederecoveryconfiguration</span><span class="sxs-lookup"><span data-stu-id="9506a-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9506a-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="9506a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
