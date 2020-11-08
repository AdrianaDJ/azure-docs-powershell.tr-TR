---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276632"
---
# <span data-ttu-id="9b4c5-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b4c5-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="9b4c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4c5-103">Veritabanı sunucusu kurtarma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="9b4c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b4c5-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b4c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4c5-106">**Set-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu kurtarma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="9b4c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b4c5-107">EXAMPLES</span></span>

## <span data-ttu-id="9b4c5-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b4c5-108">PARAMETERS</span></span>

### <span data-ttu-id="9b4c5-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="9b4c5-109">-AllowDataLoss</span></span>
<span data-ttu-id="9b4c5-110">Yerine çalışma işleminin veri kaybına izin verdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="9b4c5-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="9b4c5-111">-AsJob</span></span>
<span data-ttu-id="9b4c5-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9b4c5-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4c5-113">-DefaultProfile</span></span>
<span data-ttu-id="9b4c5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9b4c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b4c5-115">-Yük devretme</span><span class="sxs-lookup"><span data-stu-id="9b4c5-115">-Failover</span></span>
<span data-ttu-id="9b4c5-116">Bu işlemin bir yük devretme olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b4c5-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b4c5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9b4c5-119">-ServerName</span></span>
<span data-ttu-id="9b4c5-120">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="9b4c5-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="9b4c5-121">-VirtualEndpointName</span></span>
<span data-ttu-id="9b4c5-122">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="9b4c5-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b4c5-123">-Confirm</span></span>
<span data-ttu-id="9b4c5-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4c5-125">-WhatIf</span></span>
<span data-ttu-id="9b4c5-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b4c5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4c5-128">CommonParameters</span></span>
<span data-ttu-id="9b4c5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4c5-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b4c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4c5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b4c5-131">INPUTS</span></span>

### <span data-ttu-id="9b4c5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9b4c5-132">System.String</span></span>

## <span data-ttu-id="9b4c5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b4c5-133">OUTPUTS</span></span>

### <span data-ttu-id="9b4c5-134">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="9b4c5-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="9b4c5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b4c5-135">NOTES</span></span>

## <span data-ttu-id="9b4c5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b4c5-136">RELATED LINKS</span></span>

[<span data-ttu-id="9b4c5-137">Get-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9b4c5-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9b4c5-138">Yeni-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9b4c5-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9b4c5-139">Remove-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9b4c5-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9b4c5-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="9b4c5-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
