---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277516"
---
# <span data-ttu-id="40b52-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="40b52-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="40b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b52-102">SYNOPSIS</span></span>
<span data-ttu-id="40b52-103">Veritabanı sunucusu sistem kurtarma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="40b52-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="40b52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40b52-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40b52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40b52-105">DESCRIPTION</span></span>
<span data-ttu-id="40b52-106">**Get-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="40b52-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="40b52-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40b52-107">EXAMPLES</span></span>

## <span data-ttu-id="40b52-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40b52-108">PARAMETERS</span></span>

### <span data-ttu-id="40b52-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b52-109">-DefaultProfile</span></span>
<span data-ttu-id="40b52-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="40b52-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40b52-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b52-111">-ResourceGroupName</span></span>
<span data-ttu-id="40b52-112">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40b52-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="40b52-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40b52-113">-ServerName</span></span>
<span data-ttu-id="40b52-114">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40b52-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="40b52-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="40b52-115">-VirtualEndpointName</span></span>
<span data-ttu-id="40b52-116">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40b52-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="40b52-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="40b52-117">-Confirm</span></span>
<span data-ttu-id="40b52-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40b52-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b52-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b52-119">-WhatIf</span></span>
<span data-ttu-id="40b52-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40b52-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b52-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40b52-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b52-122">CommonParameters</span></span>
<span data-ttu-id="40b52-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40b52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b52-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40b52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b52-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40b52-125">INPUTS</span></span>

### <span data-ttu-id="40b52-126">System. String</span><span class="sxs-lookup"><span data-stu-id="40b52-126">System.String</span></span>

## <span data-ttu-id="40b52-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40b52-127">OUTPUTS</span></span>

### <span data-ttu-id="40b52-128">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="40b52-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="40b52-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40b52-129">NOTES</span></span>

## <span data-ttu-id="40b52-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40b52-130">RELATED LINKS</span></span>

[<span data-ttu-id="40b52-131">Yeni-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="40b52-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="40b52-132">Remove-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="40b52-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="40b52-133">Set-Azsqlserverdederecoveryconfiguration</span><span class="sxs-lookup"><span data-stu-id="40b52-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="40b52-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="40b52-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

