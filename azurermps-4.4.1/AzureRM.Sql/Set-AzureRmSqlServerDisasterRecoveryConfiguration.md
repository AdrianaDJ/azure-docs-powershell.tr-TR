---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765039"
---
# <span data-ttu-id="d7a71-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7a71-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d7a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7a71-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a71-103">Veritabanı sunucusu kurtarma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7a71-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7a71-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a71-106">**Set-Azurermsqlserverdeyıldız sunucum yapılandırma** CMDLET 'i SQL veritabanı sunucusu kurtarma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="d7a71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7a71-107">EXAMPLES</span></span>

## <span data-ttu-id="d7a71-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7a71-108">PARAMETERS</span></span>

### <span data-ttu-id="d7a71-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d7a71-109">-AllowDataLoss</span></span>
<span data-ttu-id="d7a71-110">Yerine çalışma işleminin veri kaybına izin verdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d7a71-111">-Yük devretme</span><span class="sxs-lookup"><span data-stu-id="d7a71-111">-Failover</span></span>
<span data-ttu-id="d7a71-112">Bu işlemin bir yük devretme olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-112">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="d7a71-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a71-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7a71-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d7a71-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7a71-115">-ServerName</span></span>
<span data-ttu-id="d7a71-116">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="d7a71-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d7a71-117">-VirtualEndpointName</span></span>
<span data-ttu-id="d7a71-118">Sanal uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="d7a71-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7a71-119">-Confirm</span></span>
<span data-ttu-id="d7a71-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7a71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a71-121">-WhatIf</span></span>
<span data-ttu-id="d7a71-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7a71-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a71-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7a71-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a71-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a71-124">-DefaultProfile</span></span>
<span data-ttu-id="d7a71-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7a71-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a71-126">CommonParameters</span></span>
<span data-ttu-id="d7a71-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7a71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a71-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a71-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a71-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7a71-129">INPUTS</span></span>

## <span data-ttu-id="d7a71-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7a71-130">OUTPUTS</span></span>

## <span data-ttu-id="d7a71-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7a71-131">NOTES</span></span>

## <span data-ttu-id="d7a71-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7a71-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7a71-133">Get-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7a71-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d7a71-134">New-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7a71-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d7a71-135">Remove-Azurermsqlserverdisyıldız yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7a71-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d7a71-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d7a71-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
