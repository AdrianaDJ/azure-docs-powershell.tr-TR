---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107555"
---
# <span data-ttu-id="5cfb8-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cfb8-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5cfb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cfb8-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfb8-103">SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5cfb8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cfb8-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cfb8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cfb8-105">DESCRIPTION</span></span>
<span data-ttu-id="5cfb8-106">**Remove-Azsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5cfb8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cfb8-107">EXAMPLES</span></span>

## <span data-ttu-id="5cfb8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cfb8-108">PARAMETERS</span></span>

### <span data-ttu-id="5cfb8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfb8-109">-DefaultProfile</span></span>
<span data-ttu-id="5cfb8-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cfb8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cfb8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5cfb8-111">-Force</span></span>
<span data-ttu-id="5cfb8-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5cfb8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cfb8-113">-ResourceGroupName</span></span>
<span data-ttu-id="5cfb8-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5cfb8-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cfb8-115">-ServerName</span></span>
<span data-ttu-id="5cfb8-116">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="5cfb8-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5cfb8-117">-VirtualEndpointName</span></span>
<span data-ttu-id="5cfb8-118">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="5cfb8-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cfb8-119">-Confirm</span></span>
<span data-ttu-id="5cfb8-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cfb8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cfb8-121">-WhatIf</span></span>
<span data-ttu-id="5cfb8-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cfb8-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cfb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfb8-124">CommonParameters</span></span>
<span data-ttu-id="5cfb8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfb8-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfb8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cfb8-127">INPUTS</span></span>

### <span data-ttu-id="5cfb8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5cfb8-128">System.String</span></span>

## <span data-ttu-id="5cfb8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cfb8-129">OUTPUTS</span></span>

### <span data-ttu-id="5cfb8-130">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="5cfb8-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="5cfb8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cfb8-131">NOTES</span></span>

## <span data-ttu-id="5cfb8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cfb8-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cfb8-133">Get-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5cfb8-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5cfb8-134">Yeni-Azsqlserverdeyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5cfb8-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5cfb8-135">Set-Azsqlserverdederecoveryconfiguration</span><span class="sxs-lookup"><span data-stu-id="5cfb8-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5cfb8-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5cfb8-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
