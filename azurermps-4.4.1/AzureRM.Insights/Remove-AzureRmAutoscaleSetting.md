---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593119"
---
# <span data-ttu-id="ca01e-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca01e-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="ca01e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca01e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca01e-103">Otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca01e-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca01e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca01e-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca01e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca01e-105">DESCRIPTION</span></span>
<span data-ttu-id="ca01e-106">**Remove-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca01e-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="ca01e-107">Ayarın adını ve atandığı kaynak grubunun adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca01e-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="ca01e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca01e-108">EXAMPLES</span></span>

## <span data-ttu-id="ca01e-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca01e-109">PARAMETERS</span></span>

### <span data-ttu-id="ca01e-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca01e-110">-Name</span></span>
<span data-ttu-id="ca01e-111">Kaldırılacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca01e-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca01e-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca01e-112">-ResourceGroup</span></span>
<span data-ttu-id="ca01e-113">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca01e-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca01e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca01e-114">-DefaultProfile</span></span>
<span data-ttu-id="ca01e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca01e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca01e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca01e-116">CommonParameters</span></span>
<span data-ttu-id="ca01e-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca01e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca01e-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca01e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca01e-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca01e-119">INPUTS</span></span>

## <span data-ttu-id="ca01e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca01e-120">OUTPUTS</span></span>

### <span data-ttu-id="ca01e-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ca01e-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ca01e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca01e-122">NOTES</span></span>

## <span data-ttu-id="ca01e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca01e-123">RELATED LINKS</span></span>

[<span data-ttu-id="ca01e-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca01e-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="ca01e-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca01e-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


