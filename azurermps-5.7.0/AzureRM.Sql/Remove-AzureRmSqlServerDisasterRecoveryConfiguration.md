---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589656"
---
# <span data-ttu-id="2f4e9-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f4e9-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2f4e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4e9-103">SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f4e9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f4e9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4e9-106">**Remove-Azurermsqlserverdisyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2f4e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f4e9-107">EXAMPLES</span></span>

## <span data-ttu-id="2f4e9-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f4e9-108">PARAMETERS</span></span>

### <span data-ttu-id="2f4e9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4e9-109">-DefaultProfile</span></span>
<span data-ttu-id="2f4e9-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2f4e9-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2f4e9-111">-Force</span></span>
<span data-ttu-id="2f4e9-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4e9-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f4e9-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-114">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f4e9-115">-ServerName</span></span>
<span data-ttu-id="2f4e9-116">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-116">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f4e9-117">-VirtualEndpointName</span></span>
<span data-ttu-id="2f4e9-118">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f4e9-119">-Confirm</span></span>
<span data-ttu-id="2f4e9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4e9-121">-WhatIf</span></span>
<span data-ttu-id="2f4e9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4e9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4e9-124">CommonParameters</span></span>
<span data-ttu-id="2f4e9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4e9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4e9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f4e9-127">INPUTS</span></span>

### <span data-ttu-id="2f4e9-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2f4e9-128">None</span></span>
<span data-ttu-id="2f4e9-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f4e9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f4e9-130">OUTPUTS</span></span>

## <span data-ttu-id="2f4e9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f4e9-131">NOTES</span></span>

## <span data-ttu-id="2f4e9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f4e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f4e9-133">Get-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2f4e9-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f4e9-134">New-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2f4e9-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f4e9-135">Set-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2f4e9-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f4e9-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="2f4e9-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
