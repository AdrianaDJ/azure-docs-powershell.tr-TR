---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 68a03059a99c8e50d5f0ae77b131fa8ab9ed6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751393"
---
# <span data-ttu-id="c6280-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c6280-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="c6280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6280-102">SYNOPSIS</span></span>
<span data-ttu-id="c6280-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6280-103">Regenerates an account key.</span></span>

## <span data-ttu-id="c6280-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6280-104">SYNTAX</span></span>

### <span data-ttu-id="c6280-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6280-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6280-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c6280-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6280-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c6280-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6280-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6280-108">DESCRIPTION</span></span>
<span data-ttu-id="c6280-109">New-AzMapsAccountKey cmdlet 'i, Azure haritalar hesabı için bir API anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6280-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="c6280-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6280-110">EXAMPLES</span></span>

### <span data-ttu-id="c6280-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6280-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="c6280-112">MyResourceGroup kaynak grubundaki MyAccount hesabı için birincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6280-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c6280-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c6280-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="c6280-114">Belirtilen Azure haritalar hesabının Ikincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6280-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c6280-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6280-115">PARAMETERS</span></span>

### <span data-ttu-id="c6280-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6280-116">-DefaultProfile</span></span>
<span data-ttu-id="c6280-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6280-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6280-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6280-118">-InputObject</span></span>
<span data-ttu-id="c6280-119">Get-AzMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="c6280-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6280-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c6280-120">-KeyName</span></span>
<span data-ttu-id="c6280-121">Harita hesap anahtarı.</span><span class="sxs-lookup"><span data-stu-id="c6280-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6280-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6280-122">-Name</span></span>
<span data-ttu-id="c6280-123">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c6280-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6280-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6280-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6280-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c6280-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6280-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c6280-126">-ResourceId</span></span>
<span data-ttu-id="c6280-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="c6280-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6280-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6280-128">-Confirm</span></span>
<span data-ttu-id="c6280-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6280-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6280-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6280-130">-WhatIf</span></span>
<span data-ttu-id="c6280-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6280-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6280-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6280-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6280-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6280-133">CommonParameters</span></span>
<span data-ttu-id="c6280-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6280-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6280-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6280-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6280-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6280-136">INPUTS</span></span>

### <span data-ttu-id="c6280-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c6280-137">System.String</span></span>

### <span data-ttu-id="c6280-138">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c6280-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c6280-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6280-139">OUTPUTS</span></span>

### <span data-ttu-id="c6280-140">Microsoft. Azure. Management. maps. modeller. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c6280-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="c6280-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6280-141">NOTES</span></span>

## <span data-ttu-id="c6280-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6280-142">RELATED LINKS</span></span>
