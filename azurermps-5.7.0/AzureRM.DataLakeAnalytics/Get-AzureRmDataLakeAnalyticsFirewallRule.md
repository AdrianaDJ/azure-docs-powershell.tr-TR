---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 49ddf65a5c32bafab32945b6d5114f65e3c59047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762018"
---
# <span data-ttu-id="0b969-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0b969-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0b969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b969-102">SYNOPSIS</span></span>
<span data-ttu-id="0b969-103">Bir veri Lake Analytics hesabından güvenlik duvarı kuralı veya güvenlik duvarı kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0b969-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b969-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b969-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b969-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b969-105">DESCRIPTION</span></span>
<span data-ttu-id="0b969-106">**Get-Azurermdatalakeanalizleri Ticsfirewallrule** cmdlet 'i, bir Azure Data Lake Analytics hesabından güvenlik duvarı kuralları veya güvenlik duvarı kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0b969-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0b969-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b969-107">EXAMPLES</span></span>

### <span data-ttu-id="0b969-108">Örnek 1: güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="0b969-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0b969-109">Bu komut "My Firewall Rule" adlı güvenlik duvarı kuralını "ContosoAdlAcct" hesabından alır</span><span class="sxs-lookup"><span data-stu-id="0b969-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="0b969-110">Örnek 2: tüm güvenlik duvarı kurallarını listeler</span><span class="sxs-lookup"><span data-stu-id="0b969-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="0b969-111">Bu komut, "ContosoAdlAcct" hesabından tüm güvenlik duvarı kurallarını alır</span><span class="sxs-lookup"><span data-stu-id="0b969-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0b969-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b969-112">PARAMETERS</span></span>

### <span data-ttu-id="0b969-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="0b969-113">-Account</span></span>
<span data-ttu-id="0b969-114">Güvenlik duvarının alınacağı bir</span><span class="sxs-lookup"><span data-stu-id="0b969-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b969-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b969-115">-DefaultProfile</span></span>
<span data-ttu-id="0b969-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0b969-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b969-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b969-117">-Name</span></span>
<span data-ttu-id="0b969-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0b969-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b969-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b969-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b969-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b969-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b969-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b969-121">CommonParameters</span></span>
<span data-ttu-id="0b969-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b969-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b969-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b969-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b969-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b969-124">INPUTS</span></span>

### <span data-ttu-id="0b969-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0b969-125">System.String</span></span>

## <span data-ttu-id="0b969-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b969-126">OUTPUTS</span></span>

### <span data-ttu-id="0b969-127">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="0b969-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="0b969-128">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataLakeAnalytics. modeller. Datalakeçözümlemeler, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0b969-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0b969-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b969-129">NOTES</span></span>

## <span data-ttu-id="0b969-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b969-130">RELATED LINKS</span></span>

