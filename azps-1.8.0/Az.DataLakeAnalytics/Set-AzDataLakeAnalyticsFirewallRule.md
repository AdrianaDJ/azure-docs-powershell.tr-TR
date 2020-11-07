---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 8d69a3297f23fdc9e4095a695ee790ae2476a136
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916943"
---
# <span data-ttu-id="66669-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66669-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="66669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66669-102">SYNOPSIS</span></span>
<span data-ttu-id="66669-103">Bir veri Lake Analytics hesabındaki güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66669-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="66669-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66669-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66669-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66669-105">DESCRIPTION</span></span>
<span data-ttu-id="66669-106">**Set-Azdatalakeanalizleri Ticsfirewallrule** cmdlet 'i, bir Azure Data Lake Analytics hesabında güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66669-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="66669-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66669-107">EXAMPLES</span></span>

### <span data-ttu-id="66669-108">Örnek 1: güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="66669-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="66669-109">Bu komut, yeni IP aralığına sahip olmak için "ContosoAdlAcct" hesabındaki "güvenlik duvarıyla</span><span class="sxs-lookup"><span data-stu-id="66669-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="66669-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66669-110">PARAMETERS</span></span>

### <span data-ttu-id="66669-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="66669-111">-Account</span></span>
<span data-ttu-id="66669-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="66669-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="66669-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66669-113">-DefaultProfile</span></span>
<span data-ttu-id="66669-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="66669-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66669-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="66669-115">-EndIpAddress</span></span>
<span data-ttu-id="66669-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="66669-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="66669-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="66669-117">-Name</span></span>
<span data-ttu-id="66669-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="66669-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="66669-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66669-119">-ResourceGroupName</span></span>
<span data-ttu-id="66669-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66669-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="66669-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="66669-121">-StartIpAddress</span></span>
<span data-ttu-id="66669-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="66669-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="66669-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="66669-123">-Confirm</span></span>
<span data-ttu-id="66669-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66669-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66669-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66669-125">-WhatIf</span></span>
<span data-ttu-id="66669-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66669-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66669-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66669-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66669-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66669-128">CommonParameters</span></span>
<span data-ttu-id="66669-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66669-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66669-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66669-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66669-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66669-131">INPUTS</span></span>

### <span data-ttu-id="66669-132">System. String</span><span class="sxs-lookup"><span data-stu-id="66669-132">System.String</span></span>

## <span data-ttu-id="66669-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66669-133">OUTPUTS</span></span>

### <span data-ttu-id="66669-134">Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanallersfirewallrule</span><span class="sxs-lookup"><span data-stu-id="66669-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="66669-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66669-135">NOTES</span></span>

## <span data-ttu-id="66669-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66669-136">RELATED LINKS</span></span>
