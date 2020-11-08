---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096699"
---
# <span data-ttu-id="37b3e-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="37b3e-101">Select-AzProfile</span></span>

## <span data-ttu-id="37b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="37b3e-103">Birden çok hizmet profilini destekleyen modüller için-verilen hizmet profiliyle ilişkili cmdlet 'leri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="37b3e-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="37b3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37b3e-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b3e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="37b3e-106">Birden çok hizmet profilini destekleyen modüller için-verilen hizmet profiliyle ilişkili cmdlet 'leri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="37b3e-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="37b3e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37b3e-107">EXAMPLES</span></span>

### <span data-ttu-id="37b3e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37b3e-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="37b3e-109">Mart 2019 ' den AzureStack profili için cmdlet 'leri yükleme</span><span class="sxs-lookup"><span data-stu-id="37b3e-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="37b3e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37b3e-110">PARAMETERS</span></span>

### <span data-ttu-id="37b3e-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="37b3e-111">-Name</span></span>
<span data-ttu-id="37b3e-112">Seçilecek profilin adı</span><span class="sxs-lookup"><span data-stu-id="37b3e-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b3e-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="37b3e-113">-PassThru</span></span>
<span data-ttu-id="37b3e-114">Varsa, cmdlet 'i başarılı bir yürütmede bir değer döndürmeye zorlar</span><span class="sxs-lookup"><span data-stu-id="37b3e-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="37b3e-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="37b3e-115">-Confirm</span></span>
<span data-ttu-id="37b3e-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37b3e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b3e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b3e-117">-WhatIf</span></span>
<span data-ttu-id="37b3e-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37b3e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b3e-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37b3e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b3e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b3e-120">CommonParameters</span></span>
<span data-ttu-id="37b3e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37b3e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b3e-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b3e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b3e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37b3e-123">INPUTS</span></span>

### <span data-ttu-id="37b3e-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37b3e-124">None</span></span>

## <span data-ttu-id="37b3e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37b3e-125">OUTPUTS</span></span>

### <span data-ttu-id="37b3e-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="37b3e-126">System.Object</span></span>
## <span data-ttu-id="37b3e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37b3e-127">NOTES</span></span>

## <span data-ttu-id="37b3e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37b3e-128">RELATED LINKS</span></span>
