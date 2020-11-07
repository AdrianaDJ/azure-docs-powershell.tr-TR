---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763804"
---
# <span data-ttu-id="9d143-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="9d143-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="9d143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d143-102">SYNOPSIS</span></span>
<span data-ttu-id="9d143-103">Güvenlik otomatik hazırlama ayarlarını alır</span><span class="sxs-lookup"><span data-stu-id="9d143-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d143-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d143-104">SYNTAX</span></span>

### <span data-ttu-id="9d143-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9d143-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d143-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9d143-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d143-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="9d143-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d143-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d143-108">DESCRIPTION</span></span>
<span data-ttu-id="9d143-109">Otomatik sağlama ayarları, Azure Güvenlik sertifikası 'nın VM 'larınıza yüklenecek bir güvenlik Aracısı proviosion</span><span class="sxs-lookup"><span data-stu-id="9d143-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="9d143-110">Güvenlik Aracısı, güvenlik uyarıları oluşturmak ve VM 'nin güvenlik uyumluluğunu izlemek için VM 'inizi izler.</span><span class="sxs-lookup"><span data-stu-id="9d143-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="9d143-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d143-111">EXAMPLES</span></span>

### <span data-ttu-id="9d143-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9d143-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="9d143-113">Aboneliğin otomatik sağlama ayarını alır</span><span class="sxs-lookup"><span data-stu-id="9d143-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="9d143-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d143-114">PARAMETERS</span></span>

### <span data-ttu-id="9d143-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d143-115">-DefaultProfile</span></span>
<span data-ttu-id="9d143-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d143-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d143-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d143-117">-Name</span></span>
<span data-ttu-id="9d143-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9d143-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d143-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9d143-119">-ResourceId</span></span>
<span data-ttu-id="9d143-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9d143-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d143-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d143-121">CommonParameters</span></span>
<span data-ttu-id="9d143-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d143-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d143-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d143-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d143-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d143-124">INPUTS</span></span>

### <span data-ttu-id="9d143-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9d143-125">System.String</span></span>

## <span data-ttu-id="9d143-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d143-126">OUTPUTS</span></span>

### <span data-ttu-id="9d143-127">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="9d143-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="9d143-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d143-128">NOTES</span></span>

## <span data-ttu-id="9d143-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d143-129">RELATED LINKS</span></span>
