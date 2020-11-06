---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 14eb3de52c08c276638c5079a1e64c65da6669f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593367"
---
# <span data-ttu-id="dcdcc-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dcdcc-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="dcdcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcdcc-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdcc-103">Azure SQL Server sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcdcc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcdcc-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcdcc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcdcc-105">DESCRIPTION</span></span>
<span data-ttu-id="dcdcc-106">Bu komut, belirli bir Azure SQL Server sanal ağ kuralını veya bir sunucu altında Azure SQL Server sanal ağ kurallarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="dcdcc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcdcc-107">EXAMPLES</span></span>

### <span data-ttu-id="dcdcc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcdcc-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="dcdcc-109">Tek bir Azure SQL Server sanal ağ kuralı alır</span><span class="sxs-lookup"><span data-stu-id="dcdcc-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="dcdcc-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dcdcc-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="dcdcc-111">Belirtilen sunucunun altındaki Azure SQL Server sanal ağ kurallarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="dcdcc-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="dcdcc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcdcc-112">PARAMETERS</span></span>

### <span data-ttu-id="dcdcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdcc-113">-DefaultProfile</span></span>
<span data-ttu-id="dcdcc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dcdcc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcdcc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdcc-115">-ResourceGroupName</span></span>
<span data-ttu-id="dcdcc-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcdcc-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcdcc-117">-ServerName</span></span>
<span data-ttu-id="dcdcc-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="dcdcc-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="dcdcc-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="dcdcc-120">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-120">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="dcdcc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdcc-121">CommonParameters</span></span>
<span data-ttu-id="dcdcc-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcdcc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdcc-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcdcc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdcc-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcdcc-124">INPUTS</span></span>

### <span data-ttu-id="dcdcc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dcdcc-125">System.String</span></span>

## <span data-ttu-id="dcdcc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcdcc-126">OUTPUTS</span></span>

### <span data-ttu-id="dcdcc-127">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="dcdcc-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="dcdcc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcdcc-128">NOTES</span></span>

## <span data-ttu-id="dcdcc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcdcc-129">RELATED LINKS</span></span>
