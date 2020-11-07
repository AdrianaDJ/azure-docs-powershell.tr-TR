---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 04b98f15def219c269bf18f21fb371822cc97f6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935229"
---
# <span data-ttu-id="bd668-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="bd668-101">Select-AzProfile</span></span>

## <span data-ttu-id="bd668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd668-102">SYNOPSIS</span></span>
<span data-ttu-id="bd668-103">Birden çok hizmet profilini destekleyen modüller için-verilen hizmet profiliyle ilişkili cmdlet 'leri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="bd668-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="bd668-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd668-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd668-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd668-105">DESCRIPTION</span></span>
<span data-ttu-id="bd668-106">Birden çok hizmet profilini destekleyen modüller için-verilen hizmet profiliyle ilişkili cmdlet 'leri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="bd668-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="bd668-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd668-107">EXAMPLES</span></span>

### <span data-ttu-id="bd668-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd668-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="bd668-109">Mart 2019 ' den AzureStack profili için cmdlet 'leri yükleme</span><span class="sxs-lookup"><span data-stu-id="bd668-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="bd668-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd668-110">PARAMETERS</span></span>

### <span data-ttu-id="bd668-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd668-111">-Name</span></span>
<span data-ttu-id="bd668-112">Seçilecek profilin adı</span><span class="sxs-lookup"><span data-stu-id="bd668-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="bd668-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bd668-113">-PassThru</span></span>
<span data-ttu-id="bd668-114">Varsa, cmdlet 'i başarılı bir yürütmede bir değer döndürmeye zorlar</span><span class="sxs-lookup"><span data-stu-id="bd668-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="bd668-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd668-115">-Confirm</span></span>
<span data-ttu-id="bd668-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd668-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd668-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd668-117">-WhatIf</span></span>
<span data-ttu-id="bd668-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd668-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd668-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd668-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd668-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd668-120">CommonParameters</span></span>
<span data-ttu-id="bd668-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd668-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd668-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bd668-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd668-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd668-123">INPUTS</span></span>

### <span data-ttu-id="bd668-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bd668-124">None</span></span>

## <span data-ttu-id="bd668-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd668-125">OUTPUTS</span></span>

### <span data-ttu-id="bd668-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="bd668-126">System.Object</span></span>
## <span data-ttu-id="bd668-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd668-127">NOTES</span></span>

## <span data-ttu-id="bd668-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd668-128">RELATED LINKS</span></span>
