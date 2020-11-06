---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591782"
---
# <span data-ttu-id="cb372-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="cb372-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="cb372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb372-102">SYNOPSIS</span></span>
<span data-ttu-id="cb372-103">Kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="cb372-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb372-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb372-104">SYNTAX</span></span>

### <span data-ttu-id="cb372-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb372-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb372-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb372-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb372-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb372-107">DESCRIPTION</span></span>
<span data-ttu-id="cb372-108">**Get-AzureRmContainerRegistryCredential** cmdlet 'i, kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="cb372-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="cb372-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb372-109">EXAMPLES</span></span>

### <span data-ttu-id="cb372-110">Örnek 1: kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="cb372-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="cb372-111">Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="cb372-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="cb372-112">`MyRegistry`Oturum açma kimlik bilgilerini almak için Yönetici Kullanıcı kapsayıcı kayıt defteri için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="cb372-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="cb372-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb372-113">PARAMETERS</span></span>

### <span data-ttu-id="cb372-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb372-114">-Name</span></span>
<span data-ttu-id="cb372-115">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="cb372-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="cb372-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="cb372-116">-Registry</span></span>
<span data-ttu-id="cb372-117">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cb372-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb372-118">-ResourceGroupName</span></span>
<span data-ttu-id="cb372-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cb372-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb372-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb372-120">-DefaultProfile</span></span>
<span data-ttu-id="cb372-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb372-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb372-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb372-122">CommonParameters</span></span>
<span data-ttu-id="cb372-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb372-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb372-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb372-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb372-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb372-125">INPUTS</span></span>

### <span data-ttu-id="cb372-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb372-126">PSContainerRegistry</span></span>
<span data-ttu-id="cb372-127">Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cb372-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="cb372-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb372-128">OUTPUTS</span></span>

### <span data-ttu-id="cb372-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="cb372-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="cb372-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb372-130">NOTES</span></span>

## <span data-ttu-id="cb372-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb372-131">RELATED LINKS</span></span>

[<span data-ttu-id="cb372-132">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb372-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="cb372-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb372-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="cb372-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="cb372-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

