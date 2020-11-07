---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 93f951632ade49949780b970e4910c98887fe863
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762311"
---
# <span data-ttu-id="40c16-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="40c16-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="40c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40c16-102">SYNOPSIS</span></span>
<span data-ttu-id="40c16-103">Bir veri Lake Analytics hesabına güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="40c16-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40c16-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40c16-105">DESCRIPTION</span></span>
<span data-ttu-id="40c16-106">**Add-Azurermdatalakeanalyzer Ticsfirewallrule** cmdlet 'ı Azure Data Lake Analytics hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="40c16-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="40c16-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40c16-107">EXAMPLES</span></span>

### <span data-ttu-id="40c16-108">Örnek 1: güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="40c16-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="40c16-109">Bu komut "ContosoAdlAcct" hesabından "My Firewall Rule" adlı güvenlik duvarı kuralını IP aralığıyla ekler: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="40c16-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="40c16-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40c16-110">PARAMETERS</span></span>

### <span data-ttu-id="40c16-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="40c16-111">-Account</span></span>
<span data-ttu-id="40c16-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="40c16-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="40c16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c16-113">-DefaultProfile</span></span>
<span data-ttu-id="40c16-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="40c16-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40c16-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="40c16-115">-EndIpAddress</span></span>
<span data-ttu-id="40c16-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="40c16-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c16-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="40c16-117">-Name</span></span>
<span data-ttu-id="40c16-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="40c16-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="40c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="40c16-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40c16-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c16-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="40c16-121">-StartIpAddress</span></span>
<span data-ttu-id="40c16-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="40c16-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c16-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="40c16-123">-Confirm</span></span>
<span data-ttu-id="40c16-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40c16-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c16-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c16-125">-WhatIf</span></span>
<span data-ttu-id="40c16-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40c16-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c16-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40c16-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c16-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c16-128">CommonParameters</span></span>
<span data-ttu-id="40c16-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40c16-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c16-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c16-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c16-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40c16-131">INPUTS</span></span>

### <span data-ttu-id="40c16-132">System. String</span><span class="sxs-lookup"><span data-stu-id="40c16-132">System.String</span></span>

## <span data-ttu-id="40c16-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40c16-133">OUTPUTS</span></span>

### <span data-ttu-id="40c16-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="40c16-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="40c16-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40c16-135">NOTES</span></span>

## <span data-ttu-id="40c16-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40c16-136">RELATED LINKS</span></span>