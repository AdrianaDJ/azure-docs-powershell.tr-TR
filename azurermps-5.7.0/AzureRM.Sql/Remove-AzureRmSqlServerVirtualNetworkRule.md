---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c0e7bc13d52633a1da5bfac2d9aec38ea3d0ee7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588723"
---
# <span data-ttu-id="ed2f8-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed2f8-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="ed2f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2f8-103">Azure SQL Server sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed2f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed2f8-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed2f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed2f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2f8-106">Bu komut bir Azure SQL Server sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="ed2f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed2f8-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2f8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed2f8-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="ed2f8-109">Var olan bir Azure SQL Server sanal ağ kuralını siler</span><span class="sxs-lookup"><span data-stu-id="ed2f8-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="ed2f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed2f8-110">PARAMETERS</span></span>

### <span data-ttu-id="ed2f8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="ed2f8-111">-AsJob</span></span>
<span data-ttu-id="ed2f8-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ed2f8-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="ed2f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2f8-113">-DefaultProfile</span></span>
<span data-ttu-id="ed2f8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ed2f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>


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

### <span data-ttu-id="ed2f8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2f8-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed2f8-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed2f8-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed2f8-117">-ServerName</span></span>
<span data-ttu-id="ed2f8-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ed2f8-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="ed2f8-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="ed2f8-120">Azure SQL Server sanal ağ kuralı adı</span><span class="sxs-lookup"><span data-stu-id="ed2f8-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="ed2f8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed2f8-121">-Confirm</span></span>
<span data-ttu-id="ed2f8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2f8-123">-WhatIf</span></span>
<span data-ttu-id="ed2f8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2f8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2f8-126">CommonParameters</span></span>
<span data-ttu-id="ed2f8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed2f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2f8-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2f8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed2f8-129">INPUTS</span></span>

### <span data-ttu-id="ed2f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ed2f8-130">System.String</span></span>

## <span data-ttu-id="ed2f8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed2f8-131">OUTPUTS</span></span>

### <span data-ttu-id="ed2f8-132">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="ed2f8-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="ed2f8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed2f8-133">NOTES</span></span>

## <span data-ttu-id="ed2f8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed2f8-134">RELATED LINKS</span></span>
