---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275114"
---
# <span data-ttu-id="dae19-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dae19-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="dae19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae19-102">SYNOPSIS</span></span>
<span data-ttu-id="dae19-103">Belirli bir Azure örneğine bağlanmak için uç noktaları ve meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dae19-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="dae19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dae19-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dae19-105">DESCRIPTION</span></span>
<span data-ttu-id="dae19-106">Remove-AzEnvironment cmdlet, belirli bir Azure örneğine bağlanmak için uç noktaları ve meta veri bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dae19-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="dae19-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dae19-107">EXAMPLES</span></span>

### <span data-ttu-id="dae19-108">Örnek 1: test ortamı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="dae19-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="dae19-109">Bu örnekte, Add-AzEnvironment kullanılarak nasıl ortam oluşturulacağı gösterilir ve ardından Remove-AzEnvironment kullanılarak ortam nasıl silinir.</span><span class="sxs-lookup"><span data-stu-id="dae19-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="dae19-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dae19-110">PARAMETERS</span></span>

### <span data-ttu-id="dae19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae19-111">-DefaultProfile</span></span>
<span data-ttu-id="dae19-112">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dae19-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dae19-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dae19-113">-Name</span></span>
<span data-ttu-id="dae19-114">Kaldırılacak ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dae19-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="dae19-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="dae19-115">-Scope</span></span>
<span data-ttu-id="dae19-116">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="dae19-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae19-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="dae19-117">-Confirm</span></span>
<span data-ttu-id="dae19-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dae19-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae19-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae19-119">-WhatIf</span></span>
<span data-ttu-id="dae19-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dae19-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dae19-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dae19-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae19-122">CommonParameters</span></span>
<span data-ttu-id="dae19-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dae19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae19-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae19-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae19-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dae19-125">INPUTS</span></span>

### <span data-ttu-id="dae19-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dae19-126">System.String</span></span>

## <span data-ttu-id="dae19-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dae19-127">OUTPUTS</span></span>

### <span data-ttu-id="dae19-128">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="dae19-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="dae19-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dae19-129">NOTES</span></span>

## <span data-ttu-id="dae19-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dae19-130">RELATED LINKS</span></span>

[<span data-ttu-id="dae19-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dae19-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="dae19-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dae19-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="dae19-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="dae19-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

