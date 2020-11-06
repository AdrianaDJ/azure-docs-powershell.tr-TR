---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 483b71d53dfb4754a4fa5f00331b07a685102782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588737"
---
# <span data-ttu-id="5f8b0-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f8b0-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5f8b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8b0-103">Veritabanı sunucusu sistem kurtarma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f8b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f8b0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f8b0-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8b0-106">**Get-Azurermsqlserverdisyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5f8b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f8b0-107">EXAMPLES</span></span>

## <span data-ttu-id="5f8b0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f8b0-108">PARAMETERS</span></span>

### <span data-ttu-id="5f8b0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8b0-109">-DefaultProfile</span></span>
<span data-ttu-id="5f8b0-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5f8b0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f8b0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8b0-111">-ResourceGroupName</span></span>
<span data-ttu-id="5f8b0-112">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5f8b0-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5f8b0-113">-ServerName</span></span>
<span data-ttu-id="5f8b0-114">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="5f8b0-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5f8b0-115">-VirtualEndpointName</span></span>
<span data-ttu-id="5f8b0-116">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8b0-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f8b0-117">-Confirm</span></span>
<span data-ttu-id="5f8b0-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8b0-119">-WhatIf</span></span>
<span data-ttu-id="5f8b0-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f8b0-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f8b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8b0-122">CommonParameters</span></span>
<span data-ttu-id="5f8b0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8b0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8b0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f8b0-125">INPUTS</span></span>

### <span data-ttu-id="5f8b0-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f8b0-126">None</span></span>
<span data-ttu-id="5f8b0-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f8b0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f8b0-128">OUTPUTS</span></span>

## <span data-ttu-id="5f8b0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f8b0-129">NOTES</span></span>

## <span data-ttu-id="5f8b0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f8b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f8b0-131">New-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5f8b0-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f8b0-132">Remove-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5f8b0-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f8b0-133">Set-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5f8b0-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5f8b0-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5f8b0-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

