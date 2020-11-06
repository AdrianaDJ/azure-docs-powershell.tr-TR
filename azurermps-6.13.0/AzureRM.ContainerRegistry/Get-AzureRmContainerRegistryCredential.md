---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572862"
---
# <span data-ttu-id="97a11-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97a11-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="97a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a11-102">SYNOPSIS</span></span>
<span data-ttu-id="97a11-103">Kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="97a11-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97a11-104">SYNTAX</span></span>

### <span data-ttu-id="97a11-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97a11-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97a11-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a11-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97a11-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="97a11-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97a11-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97a11-108">DESCRIPTION</span></span>
<span data-ttu-id="97a11-109">Get-AzureRmContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="97a11-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="97a11-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97a11-110">EXAMPLES</span></span>

### <span data-ttu-id="97a11-111">Örnek 1: kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="97a11-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="97a11-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="97a11-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="97a11-113">Yönetici kullanıcısı, \` \` oturum açma kimlik bilgilerini almak amacıyla kapsayıcı kayıt defteri myregistry için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="97a11-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="97a11-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97a11-114">PARAMETERS</span></span>

### <span data-ttu-id="97a11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a11-115">-DefaultProfile</span></span>
<span data-ttu-id="97a11-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97a11-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a11-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="97a11-117">-Name</span></span>
<span data-ttu-id="97a11-118">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="97a11-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="97a11-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="97a11-119">-Registry</span></span>
<span data-ttu-id="97a11-120">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="97a11-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="97a11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a11-121">-ResourceGroupName</span></span>
<span data-ttu-id="97a11-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="97a11-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="97a11-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97a11-123">-ResourceId</span></span>
<span data-ttu-id="97a11-124">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="97a11-124">The container registry resource id</span></span>

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

### <span data-ttu-id="97a11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a11-125">CommonParameters</span></span>
<span data-ttu-id="97a11-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97a11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a11-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a11-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a11-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97a11-128">INPUTS</span></span>

### <span data-ttu-id="97a11-129">System. String</span><span class="sxs-lookup"><span data-stu-id="97a11-129">System.String</span></span>

## <span data-ttu-id="97a11-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97a11-130">OUTPUTS</span></span>

### <span data-ttu-id="97a11-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97a11-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="97a11-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97a11-132">NOTES</span></span>

## <span data-ttu-id="97a11-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97a11-133">RELATED LINKS</span></span>

[<span data-ttu-id="97a11-134">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97a11-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="97a11-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97a11-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="97a11-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97a11-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

