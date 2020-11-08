---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106235"
---
# <span data-ttu-id="861da-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="861da-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="861da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="861da-102">SYNOPSIS</span></span>
<span data-ttu-id="861da-103">Boş bir ACL yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="861da-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="861da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="861da-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="861da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="861da-105">DESCRIPTION</span></span>
<span data-ttu-id="861da-106">**New-AzureAclConfig** cmdlet 'i boş bir erişim denetim LISTESI (ACL) yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="861da-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="861da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="861da-107">EXAMPLES</span></span>

### <span data-ttu-id="861da-108">Örnek 1: ACL yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="861da-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="861da-109">Bu komut boş bir ACL yapılandırma nesnesi oluşturur ve $Acl değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="861da-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="861da-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="861da-110">PARAMETERS</span></span>

### <span data-ttu-id="861da-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="861da-111">-InformationAction</span></span>
<span data-ttu-id="861da-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="861da-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="861da-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="861da-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="861da-114">'A</span><span class="sxs-lookup"><span data-stu-id="861da-114">Continue</span></span>
- <span data-ttu-id="861da-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="861da-115">Ignore</span></span>
- <span data-ttu-id="861da-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="861da-116">Inquire</span></span>
- <span data-ttu-id="861da-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="861da-117">SilentlyContinue</span></span>
- <span data-ttu-id="861da-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="861da-118">Stop</span></span>
- <span data-ttu-id="861da-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="861da-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861da-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="861da-120">-InformationVariable</span></span>
<span data-ttu-id="861da-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="861da-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861da-122">CommonParameters</span></span>
<span data-ttu-id="861da-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="861da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861da-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861da-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="861da-125">INPUTS</span></span>

## <span data-ttu-id="861da-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="861da-126">OUTPUTS</span></span>

## <span data-ttu-id="861da-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="861da-127">NOTES</span></span>

## <span data-ttu-id="861da-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="861da-128">RELATED LINKS</span></span>

[<span data-ttu-id="861da-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="861da-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="861da-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="861da-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="861da-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="861da-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


