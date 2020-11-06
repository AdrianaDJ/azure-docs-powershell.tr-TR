---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573386"
---
# <span data-ttu-id="fc32b-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="fc32b-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="fc32b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc32b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc32b-103">Kullanıcı tarafından geçerli bağlamda ayarlanan Varsayılanları temizler.</span><span class="sxs-lookup"><span data-stu-id="fc32b-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc32b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc32b-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc32b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc32b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc32b-106">Clear-AzureRmDefault cmdlet, Kullanıcı tarafından belirtilen geçiş parametrelerine bağlı olarak kullanıcının belirlediği Varsayılanları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc32b-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="fc32b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc32b-107">EXAMPLES</span></span>

### <span data-ttu-id="fc32b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc32b-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="fc32b-109">Bu komut, kullanıcının geçerli bağlamdaki tüm varsayılanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc32b-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="fc32b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc32b-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="fc32b-111">Bu komut, geçerli bağlamdaki Kullanıcı tarafından ayarlanan varsayılan kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc32b-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="fc32b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc32b-112">PARAMETERS</span></span>

### <span data-ttu-id="fc32b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc32b-113">-DefaultProfile</span></span>
<span data-ttu-id="fc32b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc32b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc32b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc32b-115">-Force</span></span>
<span data-ttu-id="fc32b-116">Varsayılan belirtilmemişse tüm varsayılanları kaldır</span><span class="sxs-lookup"><span data-stu-id="fc32b-116">Remove all defaults if no default is specified</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc32b-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc32b-117">-PassThru</span></span>
<span data-ttu-id="fc32b-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="fc32b-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc32b-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc32b-119">-ResourceGroup</span></span>
<span data-ttu-id="fc32b-120">Varsayılan kaynak grubunu temizle</span><span class="sxs-lookup"><span data-stu-id="fc32b-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc32b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc32b-121">-Confirm</span></span>
<span data-ttu-id="fc32b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc32b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc32b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc32b-123">-WhatIf</span></span>
<span data-ttu-id="fc32b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc32b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc32b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc32b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc32b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc32b-126">CommonParameters</span></span>
<span data-ttu-id="fc32b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc32b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc32b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc32b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc32b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc32b-129">INPUTS</span></span>

### <span data-ttu-id="fc32b-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc32b-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc32b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc32b-131">OUTPUTS</span></span>

### <span data-ttu-id="fc32b-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="fc32b-132">System.Object</span></span>

## <span data-ttu-id="fc32b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc32b-133">NOTES</span></span>

## <span data-ttu-id="fc32b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc32b-134">RELATED LINKS</span></span>

