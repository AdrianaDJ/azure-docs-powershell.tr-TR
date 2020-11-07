---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 66731d988eb0232e4223343349bec05e5a12d44b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751395"
---
# <span data-ttu-id="e586d-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e586d-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="e586d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e586d-102">SYNOPSIS</span></span>
<span data-ttu-id="e586d-103">Azure haritalar hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e586d-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="e586d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e586d-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e586d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e586d-105">DESCRIPTION</span></span>
<span data-ttu-id="e586d-106">New-AzMapsAccount cmdlet 'i belirtilen SKU ile Azure haritalar hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e586d-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="e586d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e586d-107">EXAMPLES</span></span>

### <span data-ttu-id="e586d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e586d-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e586d-109">MyResourceGroup kaynak grubunda MyAccount adlı yeni bir Azure haritalar hesabı SKU S0 ve bir etiketle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e586d-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="e586d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e586d-110">PARAMETERS</span></span>

### <span data-ttu-id="e586d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e586d-111">-DefaultProfile</span></span>
<span data-ttu-id="e586d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e586d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e586d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e586d-113">-Force</span></span>
<span data-ttu-id="e586d-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="e586d-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e586d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e586d-115">-Name</span></span>
<span data-ttu-id="e586d-116">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="e586d-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e586d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e586d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e586d-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e586d-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e586d-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e586d-119">-SkuName</span></span>
<span data-ttu-id="e586d-120">Hesap SKU adını eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="e586d-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e586d-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e586d-121">-Tag</span></span>
<span data-ttu-id="e586d-122">Hesap etiketlerini eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="e586d-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e586d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e586d-123">-Confirm</span></span>
<span data-ttu-id="e586d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e586d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e586d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e586d-125">-WhatIf</span></span>
<span data-ttu-id="e586d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e586d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e586d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e586d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e586d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e586d-128">CommonParameters</span></span>
<span data-ttu-id="e586d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e586d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e586d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e586d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e586d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e586d-131">INPUTS</span></span>

### <span data-ttu-id="e586d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e586d-132">System.String</span></span>

## <span data-ttu-id="e586d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e586d-133">OUTPUTS</span></span>

### <span data-ttu-id="e586d-134">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e586d-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e586d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e586d-135">NOTES</span></span>

## <span data-ttu-id="e586d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e586d-136">RELATED LINKS</span></span>
