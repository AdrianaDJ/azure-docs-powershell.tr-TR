---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273666"
---
# <span data-ttu-id="0f9c0-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0f9c0-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0f9c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f9c0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9c0-103">Bir veri Lake Analytics hesabına güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0f9c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f9c0-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f9c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f9c0-105">DESCRIPTION</span></span>
<span data-ttu-id="0f9c0-106">**Add-Azdatalakeanalizleri Ticsfirewallrule** cmdlet 'ı bir Azure Data Lake Analytics hesabına güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0f9c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f9c0-107">EXAMPLES</span></span>

### <span data-ttu-id="0f9c0-108">Örnek 1: güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f9c0-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="0f9c0-109">Bu komut "ContosoAdlAcct" hesabından "My Firewall Rule" adlı güvenlik duvarı kuralını IP aralığıyla ekler: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="0f9c0-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="0f9c0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f9c0-110">PARAMETERS</span></span>

### <span data-ttu-id="0f9c0-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="0f9c0-111">-Account</span></span>
<span data-ttu-id="0f9c0-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="0f9c0-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="0f9c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9c0-113">-DefaultProfile</span></span>
<span data-ttu-id="0f9c0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0f9c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f9c0-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="0f9c0-115">-EndIpAddress</span></span>
<span data-ttu-id="0f9c0-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="0f9c0-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0f9c0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f9c0-117">-Name</span></span>
<span data-ttu-id="0f9c0-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0f9c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f9c0-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="0f9c0-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="0f9c0-121">-StartIpAddress</span></span>
<span data-ttu-id="0f9c0-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="0f9c0-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0f9c0-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f9c0-123">-Confirm</span></span>
<span data-ttu-id="0f9c0-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f9c0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9c0-125">-WhatIf</span></span>
<span data-ttu-id="0f9c0-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9c0-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f9c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9c0-128">CommonParameters</span></span>
<span data-ttu-id="0f9c0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f9c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9c0-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9c0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9c0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f9c0-131">INPUTS</span></span>

### <span data-ttu-id="0f9c0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0f9c0-132">System.String</span></span>

## <span data-ttu-id="0f9c0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f9c0-133">OUTPUTS</span></span>

### <span data-ttu-id="0f9c0-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="0f9c0-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0f9c0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f9c0-135">NOTES</span></span>

## <span data-ttu-id="0f9c0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f9c0-136">RELATED LINKS</span></span>
