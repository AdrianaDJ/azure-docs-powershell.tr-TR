---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319997"
---
# <span data-ttu-id="f306a-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f306a-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="f306a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f306a-102">SYNOPSIS</span></span>
<span data-ttu-id="f306a-103">Windows sanal masaüstü kayıt bilgilerini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="f306a-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f306a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f306a-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f306a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f306a-105">DESCRIPTION</span></span>
<span data-ttu-id="f306a-106">Windows sanal masaüstü kayıt bilgilerini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="f306a-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f306a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f306a-107">EXAMPLES</span></span>

### <span data-ttu-id="f306a-108">Örnek 1: Windows sanal masaüstü kayıt belirtecini silme</span><span class="sxs-lookup"><span data-stu-id="f306a-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="f306a-109">Bu komut, bir konak havuzundaki Windows sanal masaüstü kayıt belirtecini siler.</span><span class="sxs-lookup"><span data-stu-id="f306a-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="f306a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f306a-110">PARAMETERS</span></span>

### <span data-ttu-id="f306a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f306a-111">-DefaultProfile</span></span>
<span data-ttu-id="f306a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f306a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f306a-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f306a-113">-HostPoolName</span></span>
<span data-ttu-id="f306a-114">Konak havuzu adı</span><span class="sxs-lookup"><span data-stu-id="f306a-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f306a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f306a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f306a-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f306a-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f306a-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f306a-117">-SubscriptionId</span></span>
<span data-ttu-id="f306a-118">Foo 1</span><span class="sxs-lookup"><span data-stu-id="f306a-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f306a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f306a-119">-Confirm</span></span>
<span data-ttu-id="f306a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f306a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f306a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f306a-121">-WhatIf</span></span>
<span data-ttu-id="f306a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f306a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f306a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f306a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f306a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f306a-124">CommonParameters</span></span>
<span data-ttu-id="f306a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f306a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f306a-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f306a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f306a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f306a-127">INPUTS</span></span>

## <span data-ttu-id="f306a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f306a-128">OUTPUTS</span></span>

## <span data-ttu-id="f306a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f306a-129">NOTES</span></span>

<span data-ttu-id="f306a-130">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f306a-130">ALIASES</span></span>

## <span data-ttu-id="f306a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f306a-131">RELATED LINKS</span></span>

