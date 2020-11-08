---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109022"
---
# <span data-ttu-id="a2474-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2474-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="a2474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2474-102">SYNOPSIS</span></span>
<span data-ttu-id="a2474-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI silin.</span><span class="sxs-lookup"><span data-stu-id="a2474-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a2474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2474-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2474-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2474-105">DESCRIPTION</span></span>
<span data-ttu-id="a2474-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI silin.</span><span class="sxs-lookup"><span data-stu-id="a2474-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a2474-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2474-107">EXAMPLES</span></span>

### <span data-ttu-id="a2474-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a2474-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="a2474-109">Yönetim ortağını kaldır</span><span class="sxs-lookup"><span data-stu-id="a2474-109">Remove management partner</span></span>

## <span data-ttu-id="a2474-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2474-110">PARAMETERS</span></span>

### <span data-ttu-id="a2474-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2474-111">-DefaultProfile</span></span>
<span data-ttu-id="a2474-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2474-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2474-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="a2474-113">-PartnerId</span></span>
<span data-ttu-id="a2474-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="a2474-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2474-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a2474-115">-PassThru</span></span>
<span data-ttu-id="a2474-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a2474-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2474-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2474-117">-Confirm</span></span>
<span data-ttu-id="a2474-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2474-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2474-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2474-119">-WhatIf</span></span>
<span data-ttu-id="a2474-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2474-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2474-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2474-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2474-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2474-122">CommonParameters</span></span>
<span data-ttu-id="a2474-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2474-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2474-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2474-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2474-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2474-125">INPUTS</span></span>

### <span data-ttu-id="a2474-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a2474-126">None</span></span>

## <span data-ttu-id="a2474-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2474-127">OUTPUTS</span></span>

### <span data-ttu-id="a2474-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2474-128">System.Boolean</span></span>

## <span data-ttu-id="a2474-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2474-129">NOTES</span></span>

## <span data-ttu-id="a2474-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2474-130">RELATED LINKS</span></span>

[<span data-ttu-id="a2474-131">Yeni-Azyönetim ortağı</span><span class="sxs-lookup"><span data-stu-id="a2474-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="a2474-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2474-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="a2474-133">Güncelleştirme-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2474-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)