---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937771"
---
# <span data-ttu-id="fcfe7-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fcfe7-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="fcfe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfe7-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fcfe7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcfe7-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcfe7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcfe7-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfe7-106">**Remove-AzDataLakeStoreFirewallRule** cmdlet 'ı belirtilen veri</span><span class="sxs-lookup"><span data-stu-id="fcfe7-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fcfe7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcfe7-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfe7-108">Örnek 1: bir hesaptan güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fcfe7-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="fcfe7-109">"Benimfirewallrule" güvenlik duvarı kuralını "ContosoADL" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="fcfe7-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="fcfe7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcfe7-110">PARAMETERS</span></span>

### <span data-ttu-id="fcfe7-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="fcfe7-111">-Account</span></span>
<span data-ttu-id="fcfe7-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fcfe7-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="fcfe7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfe7-113">-DefaultProfile</span></span>
<span data-ttu-id="fcfe7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fcfe7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcfe7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fcfe7-115">-Name</span></span>
<span data-ttu-id="fcfe7-116">Silinecek güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="fcfe7-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fcfe7-117">-PassThru</span></span>
<span data-ttu-id="fcfe7-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="fcfe7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfe7-119">-ResourceGroupName</span></span>
<span data-ttu-id="fcfe7-120">Güvenlik duvarının kaldırılacağı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfe7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fcfe7-121">-Confirm</span></span>
<span data-ttu-id="fcfe7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfe7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfe7-123">-WhatIf</span></span>
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

### <span data-ttu-id="fcfe7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfe7-124">CommonParameters</span></span>
<span data-ttu-id="fcfe7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcfe7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfe7-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfe7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfe7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcfe7-127">INPUTS</span></span>

### <span data-ttu-id="fcfe7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fcfe7-128">System.String</span></span>

### <span data-ttu-id="fcfe7-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcfe7-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcfe7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcfe7-130">OUTPUTS</span></span>

### <span data-ttu-id="fcfe7-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcfe7-131">System.Boolean</span></span>

## <span data-ttu-id="fcfe7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcfe7-132">NOTES</span></span>

## <span data-ttu-id="fcfe7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcfe7-133">RELATED LINKS</span></span>
