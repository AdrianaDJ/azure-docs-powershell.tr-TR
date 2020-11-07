---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592628"
---
# <span data-ttu-id="3b151-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3b151-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3b151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b151-102">SYNOPSIS</span></span>
<span data-ttu-id="3b151-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b151-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b151-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b151-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b151-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b151-105">DESCRIPTION</span></span>
<span data-ttu-id="3b151-106">**Remove-AzureRmDataLakeStoreFirewallRule** cmdlet 'ı belirtilen veri</span><span class="sxs-lookup"><span data-stu-id="3b151-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3b151-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b151-107">EXAMPLES</span></span>

### <span data-ttu-id="3b151-108">Örnek 1: bir hesaptan güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b151-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="3b151-109">"Benimfirewallrule" güvenlik duvarı kuralını "ContosoADL" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="3b151-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="3b151-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b151-110">PARAMETERS</span></span>

### <span data-ttu-id="3b151-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="3b151-111">-Account</span></span>
<span data-ttu-id="3b151-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3b151-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="3b151-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b151-113">-Name</span></span>
<span data-ttu-id="3b151-114">Silinecek güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="3b151-114">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="3b151-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3b151-115">-PassThru</span></span>
<span data-ttu-id="3b151-116">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b151-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="3b151-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b151-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b151-118">Güvenlik duvarının kaldırılacağı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b151-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="3b151-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b151-119">-Confirm</span></span>
<span data-ttu-id="3b151-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b151-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b151-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b151-121">-WhatIf</span></span>
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

### <span data-ttu-id="3b151-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b151-122">-DefaultProfile</span></span>
<span data-ttu-id="3b151-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b151-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b151-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b151-124">CommonParameters</span></span>
<span data-ttu-id="3b151-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b151-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b151-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b151-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b151-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b151-127">INPUTS</span></span>

## <span data-ttu-id="3b151-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b151-128">OUTPUTS</span></span>

### <span data-ttu-id="3b151-129">bool</span><span class="sxs-lookup"><span data-stu-id="3b151-129">bool</span></span>
<span data-ttu-id="3b151-130">Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b151-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="3b151-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b151-131">NOTES</span></span>

## <span data-ttu-id="3b151-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b151-132">RELATED LINKS</span></span>
