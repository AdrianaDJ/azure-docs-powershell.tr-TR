---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096253"
---
# <span data-ttu-id="08163-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="08163-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="08163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08163-102">SYNOPSIS</span></span>
<span data-ttu-id="08163-103">Azure SQL Server sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="08163-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="08163-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08163-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08163-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08163-105">DESCRIPTION</span></span>
<span data-ttu-id="08163-106">Bu komut, belirli bir Azure SQL Server sanal ağ kuralını veya bir sunucu altında Azure SQL Server sanal ağ kurallarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="08163-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="08163-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08163-107">EXAMPLES</span></span>

### <span data-ttu-id="08163-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08163-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="08163-109">Tek bir Azure SQL Server sanal ağ kuralı alır</span><span class="sxs-lookup"><span data-stu-id="08163-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="08163-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="08163-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="08163-111">Belirtilen sunucunun altındaki Azure SQL Server sanal ağ kurallarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="08163-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="08163-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="08163-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="08163-113">"VirtualNetworkRule" ile başlayan belirtilen sunucunun altındaki Azure SQL Server sanal ağ kurallarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="08163-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="08163-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08163-114">PARAMETERS</span></span>

### <span data-ttu-id="08163-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08163-115">-DefaultProfile</span></span>
<span data-ttu-id="08163-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="08163-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08163-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08163-117">-ResourceGroupName</span></span>
<span data-ttu-id="08163-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08163-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="08163-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08163-119">-ServerName</span></span>
<span data-ttu-id="08163-120">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="08163-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="08163-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="08163-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="08163-122">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="08163-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="08163-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08163-123">CommonParameters</span></span>
<span data-ttu-id="08163-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08163-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08163-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08163-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08163-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08163-126">INPUTS</span></span>

### <span data-ttu-id="08163-127">System. String</span><span class="sxs-lookup"><span data-stu-id="08163-127">System.String</span></span>

## <span data-ttu-id="08163-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08163-128">OUTPUTS</span></span>

### <span data-ttu-id="08163-129">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="08163-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="08163-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08163-130">NOTES</span></span>

## <span data-ttu-id="08163-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08163-131">RELATED LINKS</span></span>
