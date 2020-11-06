---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587964"
---
# <span data-ttu-id="e4f64-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e4f64-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e4f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f64-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f64-103">Bir veri Lake Analytics hesabına güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="e4f64-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4f64-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4f64-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f64-106">**Add-Azurermdatalakeanalyzer Ticsfirewallrule** cmdlet 'ı Azure Data Lake Analytics hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="e4f64-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e4f64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4f64-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f64-108">Örnek 1: güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="e4f64-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="e4f64-109">Bu komut "ContosoAdlAcct" hesabından "My Firewall Rule" adlı güvenlik duvarı kuralını IP aralığıyla ekler: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="e4f64-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="e4f64-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4f64-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f64-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e4f64-111">-Account</span></span>
<span data-ttu-id="e4f64-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="e4f64-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="e4f64-113">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="e4f64-113">-EndIpAddress</span></span>
<span data-ttu-id="e4f64-114">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="e4f64-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="e4f64-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4f64-115">-Name</span></span>
<span data-ttu-id="e4f64-116">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="e4f64-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="e4f64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f64-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4f64-118">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e4f64-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="e4f64-119">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="e4f64-119">-StartIpAddress</span></span>
<span data-ttu-id="e4f64-120">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="e4f64-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="e4f64-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4f64-121">-Confirm</span></span>
<span data-ttu-id="e4f64-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4f64-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f64-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f64-123">-WhatIf</span></span>
<span data-ttu-id="e4f64-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4f64-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f64-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4f64-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f64-126">-DefaultProfile</span></span>
<span data-ttu-id="e4f64-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4f64-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f64-128">CommonParameters</span></span>
<span data-ttu-id="e4f64-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4f64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f64-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f64-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f64-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4f64-131">INPUTS</span></span>

### <span data-ttu-id="e4f64-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f64-132">System.String</span></span>

## <span data-ttu-id="e4f64-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4f64-133">OUTPUTS</span></span>

### <span data-ttu-id="e4f64-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="e4f64-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e4f64-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4f64-135">NOTES</span></span>

## <span data-ttu-id="e4f64-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4f64-136">RELATED LINKS</span></span>

