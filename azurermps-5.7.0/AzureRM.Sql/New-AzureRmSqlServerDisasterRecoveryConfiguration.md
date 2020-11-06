---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591566"
---
# <span data-ttu-id="66300-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="66300-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="66300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66300-102">SYNOPSIS</span></span>
<span data-ttu-id="66300-103">Veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66300-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66300-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66300-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66300-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66300-105">DESCRIPTION</span></span>
<span data-ttu-id="66300-106">**Yeni-Azurermsqlserverdisyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66300-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="66300-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66300-107">EXAMPLES</span></span>

## <span data-ttu-id="66300-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66300-108">PARAMETERS</span></span>

### <span data-ttu-id="66300-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="66300-109">-AsJob</span></span>
<span data-ttu-id="66300-110">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="66300-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="66300-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66300-111">-DefaultProfile</span></span>
<span data-ttu-id="66300-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="66300-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66300-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="66300-113">-FailoverPolicy</span></span>
<span data-ttu-id="66300-114">Yerine çalışma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="66300-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66300-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="66300-116">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66300-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="66300-117">-PartnerServerName</span></span>
<span data-ttu-id="66300-118">İş ortağı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66300-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66300-119">-ResourceGroupName</span></span>
<span data-ttu-id="66300-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="66300-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66300-121">-ServerName</span></span>
<span data-ttu-id="66300-122">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="66300-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="66300-123">-VirtualEndpointName</span></span>
<span data-ttu-id="66300-124">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66300-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66300-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="66300-125">-Confirm</span></span>
<span data-ttu-id="66300-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66300-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66300-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66300-127">-WhatIf</span></span>
<span data-ttu-id="66300-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66300-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66300-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66300-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66300-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66300-130">CommonParameters</span></span>
<span data-ttu-id="66300-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66300-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66300-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66300-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66300-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66300-133">INPUTS</span></span>

### <span data-ttu-id="66300-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="66300-134">None</span></span>
<span data-ttu-id="66300-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="66300-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66300-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66300-136">OUTPUTS</span></span>

## <span data-ttu-id="66300-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66300-137">NOTES</span></span>

## <span data-ttu-id="66300-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66300-138">RELATED LINKS</span></span>

[<span data-ttu-id="66300-139">Get-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66300-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66300-140">Remove-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66300-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66300-141">Set-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66300-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66300-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="66300-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
