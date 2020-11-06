---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 7c77f11842c224a0a023215175f52bf451867296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594133"
---
# <span data-ttu-id="6dd3b-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6dd3b-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="6dd3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd3b-103">Bir öğretici hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dd3b-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd3b-106">**Remove-Azurermöğretici Iveservicesaccount** cmdlet 'ı belirtilen öğretici sitif hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="6dd3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dd3b-107">EXAMPLES</span></span>

## <span data-ttu-id="6dd3b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dd3b-108">PARAMETERS</span></span>

### <span data-ttu-id="6dd3b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd3b-109">-DefaultProfile</span></span>
<span data-ttu-id="6dd3b-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6dd3b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dd3b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6dd3b-111">-Force</span></span>
<span data-ttu-id="6dd3b-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6dd3b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6dd3b-113">-Name</span></span>
<span data-ttu-id="6dd3b-114">Silinecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-114">Specifies the name of the account to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6dd3b-116">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-116">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd3b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dd3b-117">-Confirm</span></span>
<span data-ttu-id="6dd3b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd3b-119">-WhatIf</span></span>
<span data-ttu-id="6dd3b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd3b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd3b-122">CommonParameters</span></span>
<span data-ttu-id="6dd3b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd3b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd3b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dd3b-125">INPUTS</span></span>

### <span data-ttu-id="6dd3b-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6dd3b-126">None</span></span>
<span data-ttu-id="6dd3b-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6dd3b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dd3b-128">OUTPUTS</span></span>

## <span data-ttu-id="6dd3b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dd3b-129">NOTES</span></span>

## <span data-ttu-id="6dd3b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dd3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="6dd3b-131">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="6dd3b-131">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6dd3b-132">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="6dd3b-132">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="6dd3b-133">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="6dd3b-133">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


