---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277336"
---
# <span data-ttu-id="1e065-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1e065-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="1e065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e065-102">SYNOPSIS</span></span>
<span data-ttu-id="1e065-103">Belirli bir kayıt tanımını veya kayıt tanımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1e065-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1e065-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e065-104">SYNTAX</span></span>

### <span data-ttu-id="1e065-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e065-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e065-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="1e065-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e065-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e065-107">DESCRIPTION</span></span>
<span data-ttu-id="1e065-108">Belirli bir kayıt tanımını veya kayıt tanımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1e065-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1e065-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e065-109">EXAMPLES</span></span>

### <span data-ttu-id="1e065-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e065-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1e065-111">Varsayılan kapsamdaki tüm kayıt tanımlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="1e065-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="1e065-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e065-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1e065-113">Kayıt tanımını varsayılan kapsamda adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="1e065-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="1e065-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1e065-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1e065-115">Verilen kapsamdaki tüm kayıt tanımlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="1e065-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="1e065-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e065-116">PARAMETERS</span></span>

### <span data-ttu-id="1e065-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e065-117">-DefaultProfile</span></span>
<span data-ttu-id="1e065-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e065-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e065-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e065-119">-Name</span></span>
<span data-ttu-id="1e065-120">Kayıt tanımının benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="1e065-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e065-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="1e065-121">-Scope</span></span>
<span data-ttu-id="1e065-122">Kayıt tanımının oluşturulduğu kapsam.</span><span class="sxs-lookup"><span data-stu-id="1e065-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e065-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e065-123">CommonParameters</span></span>
<span data-ttu-id="1e065-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e065-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e065-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e065-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e065-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e065-126">INPUTS</span></span>

### <span data-ttu-id="1e065-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e065-127">None</span></span>
## <span data-ttu-id="1e065-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e065-128">OUTPUTS</span></span>

### <span data-ttu-id="1e065-129">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1e065-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="1e065-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e065-130">NOTES</span></span>

## <span data-ttu-id="1e065-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e065-131">RELATED LINKS</span></span>
