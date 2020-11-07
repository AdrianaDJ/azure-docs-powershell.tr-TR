---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6d179a4cc5814c45925802f606480927a3ed3af0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761085"
---
# <span data-ttu-id="62342-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62342-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="62342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62342-102">SYNOPSIS</span></span>
<span data-ttu-id="62342-103">Bir veri Lake Analytics hesabından güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62342-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="62342-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62342-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62342-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62342-105">DESCRIPTION</span></span>
<span data-ttu-id="62342-106">**Remove-Azdatalakeanalyzer Ticsfirewallrule** cmdlet 'i, bir Azure Data Lake Analytics hesabından güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62342-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="62342-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62342-107">EXAMPLES</span></span>

### <span data-ttu-id="62342-108">Örnek 1: güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="62342-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="62342-109">Bu komut, "güvenlik duvarınız kuralı" adlı güvenlik duvarının "ContosoAdlAcct" hesabından kaldırılmasını</span><span class="sxs-lookup"><span data-stu-id="62342-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="62342-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62342-110">PARAMETERS</span></span>

### <span data-ttu-id="62342-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="62342-111">-Account</span></span>
<span data-ttu-id="62342-112">Güvenlik duvarı kuralını kaldırmak için Data Lake Analytics hesabı</span><span class="sxs-lookup"><span data-stu-id="62342-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="62342-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62342-113">-DefaultProfile</span></span>
<span data-ttu-id="62342-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="62342-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62342-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="62342-115">-Name</span></span>
<span data-ttu-id="62342-116">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="62342-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="62342-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="62342-117">-PassThru</span></span>
<span data-ttu-id="62342-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62342-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62342-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62342-119">-ResourceGroupName</span></span>
<span data-ttu-id="62342-120">Hesabı almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="62342-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="62342-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="62342-121">-Confirm</span></span>
<span data-ttu-id="62342-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62342-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62342-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62342-123">-WhatIf</span></span>
<span data-ttu-id="62342-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62342-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62342-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62342-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62342-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62342-126">CommonParameters</span></span>
<span data-ttu-id="62342-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62342-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62342-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62342-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62342-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62342-129">INPUTS</span></span>

### <span data-ttu-id="62342-130">System. String</span><span class="sxs-lookup"><span data-stu-id="62342-130">System.String</span></span>

### <span data-ttu-id="62342-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62342-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62342-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62342-132">OUTPUTS</span></span>

### <span data-ttu-id="62342-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62342-133">System.Boolean</span></span>

## <span data-ttu-id="62342-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62342-134">NOTES</span></span>

## <span data-ttu-id="62342-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62342-135">RELATED LINKS</span></span>