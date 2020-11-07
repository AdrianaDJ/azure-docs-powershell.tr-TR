---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 517f4822817a97c6ac22facb206b513a06f85d6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935849"
---
# <span data-ttu-id="2f504-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="2f504-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="2f504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f504-102">SYNOPSIS</span></span>
<span data-ttu-id="2f504-103">Tüm sertifikaları veya bir Azure IoT Hub 'ındaki belirli bir sertifikayı listeler.</span><span class="sxs-lookup"><span data-stu-id="2f504-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="2f504-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f504-104">SYNTAX</span></span>

### <span data-ttu-id="2f504-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f504-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f504-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2f504-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f504-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2f504-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f504-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f504-108">DESCRIPTION</span></span>
<span data-ttu-id="2f504-109">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2f504-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2f504-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f504-110">EXAMPLES</span></span>

### <span data-ttu-id="2f504-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f504-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2f504-112">MyIotHub 'daki tüm sertifikaları listeleme</span><span class="sxs-lookup"><span data-stu-id="2f504-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="2f504-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2f504-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="2f504-114">MyCertificate hakkında ayrıntıları göster</span><span class="sxs-lookup"><span data-stu-id="2f504-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="2f504-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f504-115">PARAMETERS</span></span>

### <span data-ttu-id="2f504-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2f504-116">-CertificateName</span></span>
<span data-ttu-id="2f504-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="2f504-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2f504-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f504-118">-DefaultProfile</span></span>
<span data-ttu-id="2f504-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f504-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f504-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f504-120">-InputObject</span></span>
<span data-ttu-id="2f504-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="2f504-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f504-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f504-122">-Name</span></span>
<span data-ttu-id="2f504-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2f504-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f504-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f504-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f504-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2f504-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f504-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2f504-126">-ResourceId</span></span>
<span data-ttu-id="2f504-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2f504-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f504-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f504-128">CommonParameters</span></span>
<span data-ttu-id="2f504-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f504-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f504-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f504-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f504-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f504-131">INPUTS</span></span>

### <span data-ttu-id="2f504-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="2f504-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2f504-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2f504-133">System.String</span></span>

## <span data-ttu-id="2f504-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f504-134">OUTPUTS</span></span>

### <span data-ttu-id="2f504-135">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="2f504-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="2f504-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f504-136">NOTES</span></span>

## <span data-ttu-id="2f504-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f504-137">RELATED LINKS</span></span>
