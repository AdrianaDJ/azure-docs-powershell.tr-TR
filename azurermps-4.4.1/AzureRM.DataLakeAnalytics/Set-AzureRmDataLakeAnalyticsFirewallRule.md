---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6f19df2f234bd66ac629f8238aa2cfea257106df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763760"
---
# <span data-ttu-id="57260-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="57260-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="57260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57260-102">SYNOPSIS</span></span>
<span data-ttu-id="57260-103">Bir veri Lake Analytics hesabındaki güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="57260-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57260-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57260-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57260-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57260-105">DESCRIPTION</span></span>
<span data-ttu-id="57260-106">**Set-Azurermdatalakeanalyzer Ticsfirewallrule** cmdlet 'i, bir Azure Data Lake Analytics hesabında bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="57260-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="57260-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57260-107">EXAMPLES</span></span>

### <span data-ttu-id="57260-108">Örnek 1: güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="57260-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="57260-109">Bu komut, yeni IP aralığına sahip olmak için "ContosoAdlAcct" hesabındaki "güvenlik duvarıyla</span><span class="sxs-lookup"><span data-stu-id="57260-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="57260-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57260-110">PARAMETERS</span></span>

### <span data-ttu-id="57260-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="57260-111">-Account</span></span>
<span data-ttu-id="57260-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="57260-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="57260-113">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="57260-113">-EndIpAddress</span></span>
<span data-ttu-id="57260-114">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="57260-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57260-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="57260-115">-Name</span></span>
<span data-ttu-id="57260-116">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="57260-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="57260-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57260-117">-ResourceGroupName</span></span>
<span data-ttu-id="57260-118">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="57260-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="57260-119">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="57260-119">-StartIpAddress</span></span>
<span data-ttu-id="57260-120">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="57260-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="57260-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="57260-121">-Confirm</span></span>
<span data-ttu-id="57260-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57260-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57260-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57260-123">-WhatIf</span></span>
<span data-ttu-id="57260-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57260-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57260-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57260-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57260-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57260-126">-DefaultProfile</span></span>
<span data-ttu-id="57260-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57260-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57260-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57260-128">CommonParameters</span></span>
<span data-ttu-id="57260-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57260-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57260-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57260-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57260-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57260-131">INPUTS</span></span>

### <span data-ttu-id="57260-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57260-132">System.String</span></span>

## <span data-ttu-id="57260-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57260-133">OUTPUTS</span></span>

### <span data-ttu-id="57260-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="57260-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="57260-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57260-135">NOTES</span></span>

## <span data-ttu-id="57260-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57260-136">RELATED LINKS</span></span>

