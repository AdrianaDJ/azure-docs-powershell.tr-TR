---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 89b3f47953c4074088c1ae5e2cf8e5f51ff383e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752612"
---
# <span data-ttu-id="4242a-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4242a-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="4242a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4242a-102">SYNOPSIS</span></span>
<span data-ttu-id="4242a-103">Kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4242a-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="4242a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4242a-104">SYNTAX</span></span>

### <span data-ttu-id="4242a-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4242a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4242a-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4242a-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4242a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4242a-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4242a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4242a-108">DESCRIPTION</span></span>
<span data-ttu-id="4242a-109">Get-AzContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4242a-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="4242a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4242a-110">EXAMPLES</span></span>

### <span data-ttu-id="4242a-111">Örnek 1: kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="4242a-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="4242a-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4242a-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="4242a-113">Yönetici kullanıcısı, \` \` oturum açma kimlik bilgilerini almak amacıyla kapsayıcı kayıt defteri myregistry için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4242a-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="4242a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4242a-114">PARAMETERS</span></span>

### <span data-ttu-id="4242a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4242a-115">-DefaultProfile</span></span>
<span data-ttu-id="4242a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4242a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4242a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4242a-117">-Name</span></span>
<span data-ttu-id="4242a-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="4242a-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4242a-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="4242a-119">-Registry</span></span>
<span data-ttu-id="4242a-120">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4242a-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4242a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4242a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4242a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4242a-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4242a-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4242a-123">-ResourceId</span></span>
<span data-ttu-id="4242a-124">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4242a-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4242a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4242a-125">CommonParameters</span></span>
<span data-ttu-id="4242a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4242a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4242a-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4242a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4242a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4242a-128">INPUTS</span></span>

### <span data-ttu-id="4242a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4242a-129">System.String</span></span>

## <span data-ttu-id="4242a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4242a-130">OUTPUTS</span></span>

### <span data-ttu-id="4242a-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4242a-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="4242a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4242a-132">NOTES</span></span>

## <span data-ttu-id="4242a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4242a-133">RELATED LINKS</span></span>

[<span data-ttu-id="4242a-134">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4242a-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="4242a-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4242a-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="4242a-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4242a-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

