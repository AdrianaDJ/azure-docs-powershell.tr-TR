---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: fbbafa000317e6cf19ed9cdde6f920aaceeaafa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759254"
---
# <span data-ttu-id="4bc63-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="4bc63-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4bc63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc63-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc63-103">Güvenlik otomatik hazırlama ayarlarını alır</span><span class="sxs-lookup"><span data-stu-id="4bc63-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="4bc63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bc63-104">SYNTAX</span></span>

### <span data-ttu-id="4bc63-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bc63-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc63-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4bc63-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bc63-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4bc63-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bc63-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bc63-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc63-109">Otomatik sağlama ayarları, Azure Güvenlik sertifikası 'nın VM 'larınıza yüklenecek bir güvenlik Aracısı proviosion</span><span class="sxs-lookup"><span data-stu-id="4bc63-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="4bc63-110">Güvenlik Aracısı, güvenlik uyarıları oluşturmak ve VM 'nin güvenlik uyumluluğunu izlemek için VM 'inizi izler.</span><span class="sxs-lookup"><span data-stu-id="4bc63-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="4bc63-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bc63-111">EXAMPLES</span></span>

### <span data-ttu-id="4bc63-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bc63-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="4bc63-113">Aboneliğin otomatik sağlama ayarını alır</span><span class="sxs-lookup"><span data-stu-id="4bc63-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="4bc63-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bc63-114">PARAMETERS</span></span>

### <span data-ttu-id="4bc63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc63-115">-DefaultProfile</span></span>
<span data-ttu-id="4bc63-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bc63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc63-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bc63-117">-Name</span></span>
<span data-ttu-id="4bc63-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4bc63-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc63-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bc63-119">-ResourceId</span></span>
<span data-ttu-id="4bc63-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4bc63-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc63-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc63-121">CommonParameters</span></span>
<span data-ttu-id="4bc63-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bc63-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc63-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc63-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc63-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bc63-124">INPUTS</span></span>

### <span data-ttu-id="4bc63-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc63-125">System.String</span></span>

## <span data-ttu-id="4bc63-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bc63-126">OUTPUTS</span></span>

### <span data-ttu-id="4bc63-127">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="4bc63-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4bc63-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bc63-128">NOTES</span></span>

## <span data-ttu-id="4bc63-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bc63-129">RELATED LINKS</span></span>
