---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587763"
---
# <span data-ttu-id="9cb80-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9cb80-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="9cb80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb80-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb80-103">Azure SQL Server sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="9cb80-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cb80-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cb80-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cb80-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb80-106">Bu komut, belirli bir Azure SQL Server sanal ağ kuralını veya bir sunucu altında Azure SQL Server sanal ağ kurallarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9cb80-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="9cb80-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cb80-107">EXAMPLES</span></span>

### <span data-ttu-id="9cb80-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cb80-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="9cb80-109">Tek bir Azure SQL Server sanal ağ kuralı alır</span><span class="sxs-lookup"><span data-stu-id="9cb80-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="9cb80-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9cb80-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="9cb80-111">Belirtilen sunucunun altındaki Azure SQL Server sanal ağ kurallarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="9cb80-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="9cb80-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cb80-112">PARAMETERS</span></span>

### <span data-ttu-id="9cb80-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb80-113">-ResourceGroupName</span></span>
<span data-ttu-id="9cb80-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9cb80-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cb80-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9cb80-115">-ServerName</span></span>
<span data-ttu-id="9cb80-116">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="9cb80-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9cb80-117">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="9cb80-117">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="9cb80-118">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="9cb80-118">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="9cb80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb80-119">-DefaultProfile</span></span>
<span data-ttu-id="9cb80-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cb80-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb80-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb80-121">CommonParameters</span></span>
<span data-ttu-id="9cb80-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cb80-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb80-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb80-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb80-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cb80-124">INPUTS</span></span>

### <span data-ttu-id="9cb80-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb80-125">System.String</span></span>

## <span data-ttu-id="9cb80-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cb80-126">OUTPUTS</span></span>

### <span data-ttu-id="9cb80-127">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="9cb80-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="9cb80-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cb80-128">NOTES</span></span>

## <span data-ttu-id="9cb80-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cb80-129">RELATED LINKS</span></span>

