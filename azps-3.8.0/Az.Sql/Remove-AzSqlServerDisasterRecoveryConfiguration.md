---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098416"
---
# <span data-ttu-id="5f56a-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f56a-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5f56a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f56a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f56a-103">SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5f56a-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5f56a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f56a-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f56a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f56a-105">DESCRIPTION</span></span>
<span data-ttu-id="5f56a-106">**Remove-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5f56a-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5f56a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f56a-107">EXAMPLES</span></span>

## <span data-ttu-id="5f56a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f56a-108">PARAMETERS</span></span>

### <span data-ttu-id="5f56a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f56a-109">-DefaultProfile</span></span>
<span data-ttu-id="5f56a-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5f56a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f56a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5f56a-111">-Force</span></span>
<span data-ttu-id="5f56a-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5f56a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f56a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f56a-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f56a-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f56a-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5f56a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5f56a-115">-ServerName</span></span>
<span data-ttu-id="5f56a-116">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f56a-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="5f56a-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5f56a-117">-VirtualEndpointName</span></span>
<span data-ttu-id="5f56a-118">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f56a-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f56a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f56a-119">-Confirm</span></span>
<span data-ttu-id="5f56a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f56a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f56a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f56a-121">-WhatIf</span></span>
<span data-ttu-id="5f56a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f56a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f56a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f56a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f56a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f56a-124">CommonParameters</span></span>
<span data-ttu-id="5f56a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f56a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f56a-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f56a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f56a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f56a-127">INPUTS</span></span>

### <span data-ttu-id="5f56a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5f56a-128">System.String</span></span>

## <span data-ttu-id="5f56a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f56a-129">OUTPUTS</span></span>

### <span data-ttu-id="5f56a-130">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="5f56a-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="5f56a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f56a-131">NOTES</span></span>

## <span data-ttu-id="5f56a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f56a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f56a-133">Get-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5f56a-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f56a-134">Yeni-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5f56a-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f56a-135">Set-Azsqlserverdederecoveryconfiguration</span><span class="sxs-lookup"><span data-stu-id="5f56a-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f56a-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5f56a-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
