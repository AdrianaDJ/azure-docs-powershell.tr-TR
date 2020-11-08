---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107414"
---
# <span data-ttu-id="31782-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="31782-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="31782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31782-102">SYNOPSIS</span></span>

## <span data-ttu-id="31782-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31782-103">SYNTAX</span></span>

### <span data-ttu-id="31782-104">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31782-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="31782-105">FromName</span><span class="sxs-lookup"><span data-stu-id="31782-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="31782-106">Fromchoparlör hizmeti</span><span class="sxs-lookup"><span data-stu-id="31782-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31782-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31782-107">DESCRIPTION</span></span>
<span data-ttu-id="31782-108">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="31782-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="31782-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="31782-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="31782-110">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="31782-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="31782-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31782-111">EXAMPLES</span></span>

### <span data-ttu-id="31782-112">Örnek 1: sanal makine rolünü alma (Portal aracılığıyla oluşturulur)</span><span class="sxs-lookup"><span data-stu-id="31782-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="31782-113">Bu komut, ContosoVMRole01 adındaki Portal aracılığıyla oluşturulan bir sanal makine rolünü alır.</span><span class="sxs-lookup"><span data-stu-id="31782-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="31782-114">Örnek 2: ad ve bulut hizmet adını kullanarak sanal makine rolü alma</span><span class="sxs-lookup"><span data-stu-id="31782-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="31782-115">Bu komut, ContosoCloudService01 adlı bir bulut hizmetinde ContosoVMRole02 adlı bir sanal makine rolünü alır.</span><span class="sxs-lookup"><span data-stu-id="31782-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="31782-116">Örnek 3: tüm sanal makine rolünü alın</span><span class="sxs-lookup"><span data-stu-id="31782-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="31782-117">Bu komut, var olan tüm sanal makine rolünü alır.</span><span class="sxs-lookup"><span data-stu-id="31782-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="31782-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31782-118">PARAMETERS</span></span>

### <span data-ttu-id="31782-119">-Cloudhizmetadı</span><span class="sxs-lookup"><span data-stu-id="31782-119">-CloudServiceName</span></span>
<span data-ttu-id="31782-120">Sanal makine rolünün bulut hizmeti adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31782-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31782-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="31782-121">-Name</span></span>
<span data-ttu-id="31782-122">Sanal makine rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31782-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31782-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="31782-123">-Profile</span></span>
<span data-ttu-id="31782-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31782-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31782-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="31782-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31782-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31782-126">CommonParameters</span></span>
<span data-ttu-id="31782-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31782-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31782-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31782-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31782-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31782-129">INPUTS</span></span>

## <span data-ttu-id="31782-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31782-130">OUTPUTS</span></span>

## <span data-ttu-id="31782-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31782-131">NOTES</span></span>

## <span data-ttu-id="31782-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31782-132">RELATED LINKS</span></span>

[<span data-ttu-id="31782-133">Yeni-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="31782-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="31782-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="31782-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="31782-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="31782-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


