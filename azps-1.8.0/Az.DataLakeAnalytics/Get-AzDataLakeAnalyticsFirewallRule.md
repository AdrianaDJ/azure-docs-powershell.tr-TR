---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 37c14547712233a025da56180e7a362f25168400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761098"
---
# <span data-ttu-id="12a90-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="12a90-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="12a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a90-102">SYNOPSIS</span></span>
<span data-ttu-id="12a90-103">Bir veri Lake Analytics hesabından güvenlik duvarı kuralı veya güvenlik duvarı kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="12a90-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="12a90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12a90-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12a90-105">DESCRIPTION</span></span>
<span data-ttu-id="12a90-106">**Get-Azdatalakeanalizleri Ticsfirewallrule** cmdlet 'i, bir Azure Data Lake Analytics hesabından güvenlik duvarı kuralı veya güvenlik duvarı kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="12a90-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="12a90-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12a90-107">EXAMPLES</span></span>

### <span data-ttu-id="12a90-108">Örnek 1: güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="12a90-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="12a90-109">Bu komut "My Firewall Rule" adlı güvenlik duvarı kuralını "ContosoAdlAcct" hesabından alır</span><span class="sxs-lookup"><span data-stu-id="12a90-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="12a90-110">Örnek 2: tüm güvenlik duvarı kurallarını listeler</span><span class="sxs-lookup"><span data-stu-id="12a90-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="12a90-111">Bu komut, "ContosoAdlAcct" hesabından tüm güvenlik duvarı kurallarını alır</span><span class="sxs-lookup"><span data-stu-id="12a90-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="12a90-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12a90-112">PARAMETERS</span></span>

### <span data-ttu-id="12a90-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="12a90-113">-Account</span></span>
<span data-ttu-id="12a90-114">Güvenlik duvarının alınacağı bir</span><span class="sxs-lookup"><span data-stu-id="12a90-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a90-115">-DefaultProfile</span></span>
<span data-ttu-id="12a90-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="12a90-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a90-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="12a90-117">-Name</span></span>
<span data-ttu-id="12a90-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="12a90-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a90-119">-ResourceGroupName</span></span>
<span data-ttu-id="12a90-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="12a90-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a90-121">CommonParameters</span></span>
<span data-ttu-id="12a90-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12a90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a90-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a90-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a90-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12a90-124">INPUTS</span></span>

### <span data-ttu-id="12a90-125">System. String</span><span class="sxs-lookup"><span data-stu-id="12a90-125">System.String</span></span>

## <span data-ttu-id="12a90-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12a90-126">OUTPUTS</span></span>

### <span data-ttu-id="12a90-127">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="12a90-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="12a90-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12a90-128">NOTES</span></span>

## <span data-ttu-id="12a90-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12a90-129">RELATED LINKS</span></span>