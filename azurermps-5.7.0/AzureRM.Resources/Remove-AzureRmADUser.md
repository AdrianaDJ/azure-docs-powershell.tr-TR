---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593439"
---
# <span data-ttu-id="4853d-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4853d-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="4853d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4853d-102">SYNOPSIS</span></span>
<span data-ttu-id="4853d-103">Active Directory kullanıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="4853d-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4853d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4853d-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4853d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4853d-105">DESCRIPTION</span></span>
<span data-ttu-id="4853d-106">Active Directory kullanıcısını (iş/okul hesabı, ayrıca org-ID olarak da bilinir) siler.</span><span class="sxs-lookup"><span data-stu-id="4853d-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4853d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4853d-107">EXAMPLES</span></span>

### <span data-ttu-id="4853d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4853d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4853d-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="4853d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4853d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4853d-110">PARAMETERS</span></span>

### <span data-ttu-id="4853d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4853d-111">-DefaultProfile</span></span>
<span data-ttu-id="4853d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4853d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4853d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4853d-113">-Force</span></span>
<span data-ttu-id="4853d-114">Belirtilmişse, Kullanıcı silme konusunda onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="4853d-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="4853d-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4853d-115">-UPNOrObjectId</span></span>
<span data-ttu-id="4853d-116">Silinecek kullanıcının Kullanıcı asıl adı veya ObjectID.</span><span class="sxs-lookup"><span data-stu-id="4853d-116">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4853d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4853d-117">-Confirm</span></span>
<span data-ttu-id="4853d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4853d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4853d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4853d-119">-WhatIf</span></span>
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

### <span data-ttu-id="4853d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4853d-120">CommonParameters</span></span>
<span data-ttu-id="4853d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4853d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4853d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4853d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4853d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4853d-123">INPUTS</span></span>

### <span data-ttu-id="4853d-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4853d-124">None</span></span>
<span data-ttu-id="4853d-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4853d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4853d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4853d-126">OUTPUTS</span></span>

## <span data-ttu-id="4853d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4853d-127">NOTES</span></span>

## <span data-ttu-id="4853d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4853d-128">RELATED LINKS</span></span>

[<span data-ttu-id="4853d-129">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4853d-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="4853d-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4853d-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="4853d-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4853d-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

