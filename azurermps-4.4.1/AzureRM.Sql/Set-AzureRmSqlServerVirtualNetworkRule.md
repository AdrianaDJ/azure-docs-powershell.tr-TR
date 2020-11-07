---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765028"
---
# <span data-ttu-id="324ad-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="324ad-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="324ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="324ad-102">SYNOPSIS</span></span>
<span data-ttu-id="324ad-103">Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="324ad-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="324ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="324ad-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="324ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="324ad-105">DESCRIPTION</span></span>
<span data-ttu-id="324ad-106">Bu komut, Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="324ad-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="324ad-107">Sunucudaki sanal ağ kuralları kümesini denetlemek için bunun yerine ' Add-AzureRmSqlServerVirtualNetworkRule ' ve ' Remove-AzureRmSqlServerVirtualNetworkRule ' seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="324ad-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="324ad-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="324ad-108">EXAMPLES</span></span>

### <span data-ttu-id="324ad-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="324ad-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="324ad-110">Yeni sanal ağ hakkında bilgi içeren yeni sanal ağ alt ağı kimliği ile mevcut bir sanal ağ kuralını değiştirir</span><span class="sxs-lookup"><span data-stu-id="324ad-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="324ad-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="324ad-111">PARAMETERS</span></span>

### <span data-ttu-id="324ad-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="324ad-112">-ResourceGroupName</span></span>
<span data-ttu-id="324ad-113">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="324ad-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="324ad-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="324ad-114">-ServerName</span></span>
<span data-ttu-id="324ad-115">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="324ad-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="324ad-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="324ad-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="324ad-117">Azure SQL Server sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="324ad-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="324ad-118">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="324ad-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="324ad-119">Kuralın sanal ağ alt ağı kimliği.</span><span class="sxs-lookup"><span data-stu-id="324ad-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="324ad-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="324ad-120">-Confirm</span></span>
<span data-ttu-id="324ad-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="324ad-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ad-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324ad-122">-WhatIf</span></span>
<span data-ttu-id="324ad-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="324ad-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="324ad-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="324ad-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324ad-125">-DefaultProfile</span></span>
<span data-ttu-id="324ad-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="324ad-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="324ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324ad-127">CommonParameters</span></span>
<span data-ttu-id="324ad-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="324ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324ad-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324ad-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="324ad-130">INPUTS</span></span>

### <span data-ttu-id="324ad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="324ad-131">System.String</span></span>

## <span data-ttu-id="324ad-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="324ad-132">OUTPUTS</span></span>

### <span data-ttu-id="324ad-133">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="324ad-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="324ad-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="324ad-134">NOTES</span></span>

## <span data-ttu-id="324ad-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="324ad-135">RELATED LINKS</span></span>

