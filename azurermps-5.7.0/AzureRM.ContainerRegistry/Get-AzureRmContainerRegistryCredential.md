---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594103"
---
# <span data-ttu-id="b08d1-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="b08d1-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="b08d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b08d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b08d1-103">Kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b08d1-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b08d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b08d1-104">SYNTAX</span></span>

### <span data-ttu-id="b08d1-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b08d1-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b08d1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b08d1-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b08d1-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b08d1-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b08d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b08d1-108">DESCRIPTION</span></span>
<span data-ttu-id="b08d1-109">Get-AzureRmContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b08d1-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="b08d1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b08d1-110">EXAMPLES</span></span>

### <span data-ttu-id="b08d1-111">Örnek 1: kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="b08d1-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="b08d1-112">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b08d1-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="b08d1-113">Yönetici kullanıcısı, \` \` oturum açma kimlik bilgilerini almak amacıyla kapsayıcı kayıt defteri myregistry için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b08d1-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="b08d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b08d1-114">PARAMETERS</span></span>

### <span data-ttu-id="b08d1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b08d1-115">-Name</span></span>
<span data-ttu-id="b08d1-116">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="b08d1-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d1-117">-Registry</span><span class="sxs-lookup"><span data-stu-id="b08d1-117">-Registry</span></span>
<span data-ttu-id="b08d1-118">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b08d1-118">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="b08d1-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b08d1-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08d1-121">-DefaultProfile</span></span>
<span data-ttu-id="b08d1-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b08d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d1-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b08d1-123">-ResourceId</span></span>
<span data-ttu-id="b08d1-124">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b08d1-124">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b08d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08d1-125">CommonParameters</span></span>
<span data-ttu-id="b08d1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b08d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08d1-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b08d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08d1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b08d1-128">INPUTS</span></span>

### <span data-ttu-id="b08d1-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b08d1-129">PSContainerRegistry</span></span>
<span data-ttu-id="b08d1-130">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b08d1-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="b08d1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b08d1-131">OUTPUTS</span></span>

### <span data-ttu-id="b08d1-132">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="b08d1-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="b08d1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b08d1-133">NOTES</span></span>

## <span data-ttu-id="b08d1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b08d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="b08d1-135">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b08d1-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="b08d1-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b08d1-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="b08d1-137">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="b08d1-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

