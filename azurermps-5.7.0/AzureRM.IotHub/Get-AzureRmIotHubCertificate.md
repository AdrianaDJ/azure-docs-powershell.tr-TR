---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 6b537811f47399d3be6b5d6485a492f7623a84c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590469"
---
# <span data-ttu-id="ba19e-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="ba19e-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="ba19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba19e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba19e-103">Tüm sertifikaları veya bir Azure IoT Hub 'ındaki belirli bir sertifikayı listeler.</span><span class="sxs-lookup"><span data-stu-id="ba19e-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba19e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba19e-104">SYNTAX</span></span>

### <span data-ttu-id="ba19e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba19e-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba19e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="ba19e-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba19e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="ba19e-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba19e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba19e-108">DESCRIPTION</span></span>
<span data-ttu-id="ba19e-109">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ba19e-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ba19e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba19e-110">EXAMPLES</span></span>

### <span data-ttu-id="ba19e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba19e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="ba19e-112">MyIotHub 'daki tüm sertifikaları listeleme</span><span class="sxs-lookup"><span data-stu-id="ba19e-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="ba19e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ba19e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="ba19e-114">MyCertificate hakkında ayrıntıları göster</span><span class="sxs-lookup"><span data-stu-id="ba19e-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="ba19e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba19e-115">PARAMETERS</span></span>

### <span data-ttu-id="ba19e-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ba19e-116">-CertificateName</span></span>
<span data-ttu-id="ba19e-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="ba19e-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba19e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba19e-118">-DefaultProfile</span></span>
<span data-ttu-id="ba19e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba19e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba19e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba19e-120">-InputObject</span></span>
<span data-ttu-id="ba19e-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="ba19e-121">IotHub Object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba19e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba19e-122">-Name</span></span>
<span data-ttu-id="ba19e-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="ba19e-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba19e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba19e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba19e-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ba19e-125">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba19e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ba19e-126">-ResourceId</span></span>
<span data-ttu-id="ba19e-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ba19e-127">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba19e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba19e-128">CommonParameters</span></span>
<span data-ttu-id="ba19e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba19e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba19e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba19e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba19e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba19e-131">INPUTS</span></span>

### <span data-ttu-id="ba19e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba19e-132">System.String</span></span>

## <span data-ttu-id="ba19e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba19e-133">OUTPUTS</span></span>

### <span data-ttu-id="ba19e-134">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="ba19e-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="ba19e-135">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription, Microsoft. Azure. Commands. IotHub, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ba19e-135">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription, Microsoft.Azure.Commands.IotHub, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ba19e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba19e-136">NOTES</span></span>

## <span data-ttu-id="ba19e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba19e-137">RELATED LINKS</span></span>

