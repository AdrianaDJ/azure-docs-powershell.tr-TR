---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764594"
---
# <span data-ttu-id="09ecf-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="09ecf-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="09ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="09ecf-103">SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="09ecf-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ecf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09ecf-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ecf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="09ecf-106">**Remove-Azurermsqlserverdisyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="09ecf-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="09ecf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09ecf-107">EXAMPLES</span></span>

## <span data-ttu-id="09ecf-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09ecf-108">PARAMETERS</span></span>

### <span data-ttu-id="09ecf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ecf-109">-DefaultProfile</span></span>
<span data-ttu-id="09ecf-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="09ecf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ecf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="09ecf-111">-Force</span></span>
<span data-ttu-id="09ecf-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="09ecf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09ecf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ecf-113">-ResourceGroupName</span></span>
<span data-ttu-id="09ecf-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ecf-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09ecf-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09ecf-115">-ServerName</span></span>
<span data-ttu-id="09ecf-116">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ecf-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="09ecf-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="09ecf-117">-VirtualEndpointName</span></span>
<span data-ttu-id="09ecf-118">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09ecf-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="09ecf-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="09ecf-119">-Confirm</span></span>
<span data-ttu-id="09ecf-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09ecf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ecf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ecf-121">-WhatIf</span></span>
<span data-ttu-id="09ecf-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ecf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ecf-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09ecf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ecf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ecf-124">CommonParameters</span></span>
<span data-ttu-id="09ecf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09ecf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ecf-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ecf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ecf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09ecf-127">INPUTS</span></span>

### <span data-ttu-id="09ecf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09ecf-128">System.String</span></span>

## <span data-ttu-id="09ecf-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09ecf-129">OUTPUTS</span></span>

### <span data-ttu-id="09ecf-130">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. azures, Serverdisderecoveryconfigurationmodel</span><span class="sxs-lookup"><span data-stu-id="09ecf-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="09ecf-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09ecf-131">NOTES</span></span>

## <span data-ttu-id="09ecf-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09ecf-132">RELATED LINKS</span></span>

[<span data-ttu-id="09ecf-133">Get-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="09ecf-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09ecf-134">New-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="09ecf-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09ecf-135">Set-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="09ecf-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09ecf-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="09ecf-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
