---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587747"
---
# <span data-ttu-id="2615c-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2615c-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2615c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2615c-102">SYNOPSIS</span></span>
<span data-ttu-id="2615c-103">Veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2615c-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2615c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2615c-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2615c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2615c-105">DESCRIPTION</span></span>
<span data-ttu-id="2615c-106">**Yeni-Azurermsqlserverdisyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2615c-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2615c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2615c-107">EXAMPLES</span></span>

## <span data-ttu-id="2615c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2615c-108">PARAMETERS</span></span>

### <span data-ttu-id="2615c-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="2615c-109">-FailoverPolicy</span></span>
<span data-ttu-id="2615c-110">Yerine çalışma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-110">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="2615c-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2615c-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2615c-112">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="2615c-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2615c-113">-PartnerServerName</span></span>
<span data-ttu-id="2615c-114">İş ortağı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="2615c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2615c-115">-ResourceGroupName</span></span>
<span data-ttu-id="2615c-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2615c-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2615c-117">-ServerName</span></span>
<span data-ttu-id="2615c-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2615c-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2615c-119">-VirtualEndpointName</span></span>
<span data-ttu-id="2615c-120">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2615c-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="2615c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2615c-121">-Confirm</span></span>
<span data-ttu-id="2615c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2615c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2615c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2615c-123">-WhatIf</span></span>
<span data-ttu-id="2615c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2615c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2615c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2615c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2615c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2615c-126">-DefaultProfile</span></span>
<span data-ttu-id="2615c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2615c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2615c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2615c-128">CommonParameters</span></span>
<span data-ttu-id="2615c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2615c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2615c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2615c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2615c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2615c-131">INPUTS</span></span>

## <span data-ttu-id="2615c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2615c-132">OUTPUTS</span></span>

## <span data-ttu-id="2615c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2615c-133">NOTES</span></span>

## <span data-ttu-id="2615c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2615c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2615c-135">Get-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2615c-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2615c-136">Remove-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2615c-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2615c-137">Set-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2615c-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2615c-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="2615c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
