---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 922c7e7055c51990b28b472805a68563c94b3e6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594780"
---
# <span data-ttu-id="fd2fa-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="fd2fa-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="fd2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2fa-103">Bir sanal makinede SQL Server Anahtar Kasası kimlik bilgileri için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd2fa-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd2fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd2fa-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd2fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd2fa-105">DESCRIPTION</span></span>

## <span data-ttu-id="fd2fa-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd2fa-106">EXAMPLES</span></span>

## <span data-ttu-id="fd2fa-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd2fa-107">PARAMETERS</span></span>

### <span data-ttu-id="fd2fa-108">-Enable</span><span class="sxs-lookup"><span data-stu-id="fd2fa-108">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fd2fa-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-110">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="fd2fa-110">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-111">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd2fa-111">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-112">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="fd2fa-112">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd2fa-113">-Profile</span></span>
<span data-ttu-id="fd2fa-114">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="fd2fa-114">@{Text=}</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fd2fa-115">-InformationAction</span></span>
<span data-ttu-id="fd2fa-116">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="fd2fa-116">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-117">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fd2fa-117">-InformationVariable</span></span>
<span data-ttu-id="fd2fa-118">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="fd2fa-118">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2fa-119">CommonParameters</span></span>
<span data-ttu-id="fd2fa-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd2fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2fa-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd2fa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2fa-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd2fa-122">INPUTS</span></span>

## <span data-ttu-id="fd2fa-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd2fa-123">OUTPUTS</span></span>

## <span data-ttu-id="fd2fa-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd2fa-124">NOTES</span></span>

## <span data-ttu-id="fd2fa-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd2fa-125">RELATED LINKS</span></span>

